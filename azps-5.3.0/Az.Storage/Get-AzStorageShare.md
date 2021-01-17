---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FD3A0013-4365-4E65-891C-5C50A9D5658C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShare.md
ms.openlocfilehash: b6323cd751d25038ff6705cee45594796d782326
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374001"
---
# <span data-ttu-id="e1f9e-101">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="e1f9e-101">Get-AzStorageShare</span></span>

## <span data-ttu-id="e1f9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1f9e-102">SYNOPSIS</span></span>
<span data-ttu-id="e1f9e-103">Ruft eine Liste der Dateifreigaben ab.</span><span class="sxs-lookup"><span data-stu-id="e1f9e-103">Gets a list of file shares.</span></span>

## <span data-ttu-id="e1f9e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e1f9e-104">SYNTAX</span></span>

### <span data-ttu-id="e1f9e-105">MatchingPrefix (Standard)</span><span class="sxs-lookup"><span data-stu-id="e1f9e-105">MatchingPrefix (Default)</span></span>
```
Get-AzStorageShare [[-Prefix] <String>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="e1f9e-106">Spezifisch</span><span class="sxs-lookup"><span data-stu-id="e1f9e-106">Specific</span></span>
```
Get-AzStorageShare [-Name] <String> [[-SnapshotTime] <DateTimeOffset>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="e1f9e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e1f9e-107">DESCRIPTION</span></span>
<span data-ttu-id="e1f9e-108">Das **Cmdlet "Get-AzStorageShare"** ruft eine Liste der Dateifreigaben für ein Speicherkonto ab.</span><span class="sxs-lookup"><span data-stu-id="e1f9e-108">The **Get-AzStorageShare** cmdlet gets a list of file shares for a storage account.</span></span>

## <span data-ttu-id="e1f9e-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e1f9e-109">EXAMPLES</span></span>

### <span data-ttu-id="e1f9e-110">Beispiel 1: Herunterladen einer Dateifreigabe</span><span class="sxs-lookup"><span data-stu-id="e1f9e-110">Example 1: Get a file share</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="e1f9e-111">Dieser Befehl ruft die Dateifreigabe "ContosoShare06" ab.</span><span class="sxs-lookup"><span data-stu-id="e1f9e-111">This command gets the file share named ContosoShare06.</span></span>

### <span data-ttu-id="e1f9e-112">Beispiel 2: Alle Dateifreigaben erhalten, die mit einer Zeichenfolge beginnen</span><span class="sxs-lookup"><span data-stu-id="e1f9e-112">Example 2: Get all file shares that begin with a string</span></span>
```
PS C:\>Get-AzStorageShare -Prefix "Contoso"
```

<span data-ttu-id="e1f9e-113">Dieser Befehl ruft alle Dateifreigaben ab, deren Namen mit Contoso beginnen.</span><span class="sxs-lookup"><span data-stu-id="e1f9e-113">This command gets all file shares that have names that begin with Contoso.</span></span>

### <span data-ttu-id="e1f9e-114">Beispiel 3: Alle Dateifreigaben in einem angegebenen Kontext erhalten</span><span class="sxs-lookup"><span data-stu-id="e1f9e-114">Example 3: Get all file shares in a specified context</span></span>
```
PS C:\>$Context = New-AzStorageContext -Local
PS C:\> Get-AzStorageShare -Context $Context
```

<span data-ttu-id="e1f9e-115">Der erste Befehl verwendet das **Cmdlet "New-AzStorageContext",** um mithilfe des Parameters *"Local"* einen Kontext zu erstellen, und speichert dieses Kontextobjekt dann in der $Context Variable.</span><span class="sxs-lookup"><span data-stu-id="e1f9e-115">The first command uses the **New-AzStorageContext** cmdlet to create a context by using the *Local* parameter, and then stores that context object in the $Context variable.</span></span>
<span data-ttu-id="e1f9e-116">Der zweite Befehl ruft die Dateifreigaben für das in der Datei gespeicherte Kontextobjekt $Context.</span><span class="sxs-lookup"><span data-stu-id="e1f9e-116">The second command gets the file shares for the context object stored in $Context.</span></span>

### <span data-ttu-id="e1f9e-117">Beispiel 4: Erhalten einer Momentaufnahme für die Dateifreigabe mit einem bestimmten Freigabenamen und SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="e1f9e-117">Example 4: Get a file share snapshot with specific share name and SnapshotTime</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" -SnapshotTime "6/16/2017 9:48:41 AM +00:00"
```

<span data-ttu-id="e1f9e-118">Dieser Befehl ruft eine Momentaufnahme der Dateifreigabe mit einem bestimmten Freigabenamen und SnapshotTime ab.</span><span class="sxs-lookup"><span data-stu-id="e1f9e-118">This command gets a file share snapshot with specific share name and SnapshotTime.</span></span>

## <span data-ttu-id="e1f9e-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1f9e-119">PARAMETERS</span></span>

### <span data-ttu-id="e1f9e-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e1f9e-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e1f9e-121">Gibt das clientseitige Zeitintervall (in Sekunden) für eine Serviceanfrage an.</span><span class="sxs-lookup"><span data-stu-id="e1f9e-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e1f9e-122">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e1f9e-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e1f9e-123">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="e1f9e-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e1f9e-124">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e1f9e-124">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e1f9e-125">Gibt die maximalen gleichzeitigen Netzwerkanrufe an.</span><span class="sxs-lookup"><span data-stu-id="e1f9e-125">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="e1f9e-126">Sie können diesen Parameter verwenden, um die Parallelität zum Drosseln der lokalen CPU- und Bandbreitenverwendung zu beschränken, indem Sie die maximale Anzahl gleichzeitiger Netzwerkaufrufe angeben.</span><span class="sxs-lookup"><span data-stu-id="e1f9e-126">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="e1f9e-127">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Anzahl der Kernwerte multipliziert.</span><span class="sxs-lookup"><span data-stu-id="e1f9e-127">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="e1f9e-128">Dieser Parameter kann zur Verringerung von Netzwerkverbindungsproblemen in Umgebungen mit geringer Bandbreite beitragen, z. B. 100 Kilobit pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="e1f9e-128">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="e1f9e-129">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="e1f9e-129">The default value is 10.</span></span>

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

### <span data-ttu-id="e1f9e-130">-Context</span><span class="sxs-lookup"><span data-stu-id="e1f9e-130">-Context</span></span>
<span data-ttu-id="e1f9e-131">Gibt einen Azure Storage-Kontext an.</span><span class="sxs-lookup"><span data-stu-id="e1f9e-131">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="e1f9e-132">Verwenden Sie zum Abrufen eines Kontexts das [Cmdlet "New-AzStorageContext".](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="e1f9e-132">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="e1f9e-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1f9e-133">-DefaultProfile</span></span>
<span data-ttu-id="e1f9e-134">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e1f9e-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1f9e-135">-Name</span><span class="sxs-lookup"><span data-stu-id="e1f9e-135">-Name</span></span>
<span data-ttu-id="e1f9e-136">Gibt den Namen der Dateifreigabe an.</span><span class="sxs-lookup"><span data-stu-id="e1f9e-136">Specifies the name of the file share.</span></span>
<span data-ttu-id="e1f9e-137">Dieses Cmdlet ruft die Dateifreigabe ab, die dieser Parameter angibt, oder nichts, wenn Sie den Namen einer Dateifreigabe angeben, die nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e1f9e-137">This cmdlet gets the file share that this parameter specifies, or nothing if you specify the name of a file share that does not exist.</span></span>

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

### <span data-ttu-id="e1f9e-138">-Prefix</span><span class="sxs-lookup"><span data-stu-id="e1f9e-138">-Prefix</span></span>
<span data-ttu-id="e1f9e-139">Gibt das Präfix für Dateifreigaben an.</span><span class="sxs-lookup"><span data-stu-id="e1f9e-139">Specifies the prefix for file shares.</span></span>
<span data-ttu-id="e1f9e-140">Dieses Cmdlet ruft Dateifreigaben ab, die dem von diesem Parameter angegebenen Präfix entsprechen, oder keine Dateifreigaben, wenn keine Dateifreigaben dem angegebenen Präfix entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e1f9e-140">This cmdlet gets file shares that match the prefix that this parameter specifies, or no file shares if no file shares match the specified prefix.</span></span>

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

### <span data-ttu-id="e1f9e-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e1f9e-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e1f9e-142">Gibt die Länge des Zeitzeitraums für den Serverteil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="e1f9e-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="e1f9e-143">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="e1f9e-143">-SnapshotTime</span></span>
<span data-ttu-id="e1f9e-144">SnapshotTime der Momentaufnahme der Dateifreigabe, die empfangen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e1f9e-144">SnapshotTime of the file share snapshot to be received.</span></span>

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

### <span data-ttu-id="e1f9e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1f9e-145">CommonParameters</span></span>
<span data-ttu-id="e1f9e-146">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1f9e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1f9e-147">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1f9e-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1f9e-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e1f9e-148">INPUTS</span></span>

### <span data-ttu-id="e1f9e-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e1f9e-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e1f9e-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e1f9e-150">OUTPUTS</span></span>

### <span data-ttu-id="e1f9e-151">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span><span class="sxs-lookup"><span data-stu-id="e1f9e-151">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span></span>

## <span data-ttu-id="e1f9e-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e1f9e-152">NOTES</span></span>

## <span data-ttu-id="e1f9e-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e1f9e-153">RELATED LINKS</span></span>

[<span data-ttu-id="e1f9e-154">New-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="e1f9e-154">New-AzStorageShare</span></span>](./New-AzStorageShare.md)

[<span data-ttu-id="e1f9e-155">Remove-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="e1f9e-155">Remove-AzStorageShare</span></span>](./Remove-AzStorageShare.md)
