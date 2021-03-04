---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 65962F9A-CC79-4B8B-9208-A993708FD36F
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageDirectory.md
ms.openlocfilehash: 6f44f1545eea4e515064873cdc77f8b34819fabc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944513"
---
# <span data-ttu-id="3bdc0-101">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="3bdc0-101">New-AzStorageDirectory</span></span>

## <span data-ttu-id="3bdc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bdc0-102">SYNOPSIS</span></span>
<span data-ttu-id="3bdc0-103">Erstellt ein Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-103">Creates a directory.</span></span>

## <span data-ttu-id="3bdc0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3bdc0-104">SYNTAX</span></span>

### <span data-ttu-id="3bdc0-105">ShareName (Standard)</span><span class="sxs-lookup"><span data-stu-id="3bdc0-105">ShareName (Default)</span></span>
```
New-AzStorageDirectory [-ShareName] <String> [-Path] <String> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="3bdc0-106">Freigeben</span><span class="sxs-lookup"><span data-stu-id="3bdc0-106">Share</span></span>
```
New-AzStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="3bdc0-107">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="3bdc0-107">Directory</span></span>
```
New-AzStorageDirectory [-Directory] <CloudFileDirectory> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="3bdc0-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3bdc0-108">DESCRIPTION</span></span>
<span data-ttu-id="3bdc0-109">Das **Cmdlet New-AzStorageDirectory** erstellt ein Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-109">The **New-AzStorageDirectory** cmdlet creates a directory.</span></span>
<span data-ttu-id="3bdc0-110">Dieses Cmdlet gibt ein **CloudFileDirectory-Objekt** zurück.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-110">This cmdlet returns a **CloudFileDirectory** object.</span></span>

## <span data-ttu-id="3bdc0-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3bdc0-111">EXAMPLES</span></span>

### <span data-ttu-id="3bdc0-112">Beispiel 1: Erstellen eines Ordners in einer Dateifreigabe</span><span class="sxs-lookup"><span data-stu-id="3bdc0-112">Example 1: Create a folder in a file share</span></span>
```
PS C:\>New-AzStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="3bdc0-113">Mit diesem Befehl wird ein Ordner namens ContosoWorkingFolder in der Dateifreigabe namens ContosoShare06 erstellt.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-113">This command creates a folder named ContosoWorkingFolder in the file share named ContosoShare06.</span></span>

### <span data-ttu-id="3bdc0-114">Beispiel 2: Erstellen eines Ordners in einer Dateifreigabe, die in einem Dateifreigabeobjekt angegeben ist</span><span class="sxs-lookup"><span data-stu-id="3bdc0-114">Example 2: Create a folder in a file share specified in a file share object</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" | New-AzStorageDirectory -Path "ContosoWorkingFolder"
```

<span data-ttu-id="3bdc0-115">Dieser Befehl verwendet das **Get-AzStorageShare-Cmdlet,** um die Dateifreigabe namens ContosoShare06 zu erhalten, und übergibt sie dann mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-115">This command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3bdc0-116">Das aktuelle Cmdlet erstellt den Ordner "ContosoWorkingFolder" in ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-116">The current cmdlet creates the folder named ContosoWorkingFolder in ContosoShare06.</span></span>

## <span data-ttu-id="3bdc0-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3bdc0-117">PARAMETERS</span></span>

### <span data-ttu-id="3bdc0-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3bdc0-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3bdc0-119">Gibt das clientseitige Zeitintervall in Sekunden für eine Dienstanforderung an.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3bdc0-120">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3bdc0-121">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="3bdc0-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3bdc0-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3bdc0-123">Gibt die maximalen gleichzeitigen Netzwerkanrufe an.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="3bdc0-124">Mit diesem Parameter können Sie die Parallelität einschränken, um die lokale CPU- und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl gleichzeitiger Netzwerkaufrufe angeben.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="3bdc0-125">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="3bdc0-126">Dieser Parameter kann dazu beitragen, Netzwerkverbindungsprobleme in Umgebungen mit geringer Bandbreite zu verringern, z. B. 100 Kilobit pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="3bdc0-127">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-127">The default value is 10.</span></span>

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

### <span data-ttu-id="3bdc0-128">-Context</span><span class="sxs-lookup"><span data-stu-id="3bdc0-128">-Context</span></span>
<span data-ttu-id="3bdc0-129">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3bdc0-130">Verwenden Sie zum Abrufen eines Speicherkontexts [das Cmdlet New-AzStorageContext.](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="3bdc0-130">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3bdc0-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bdc0-131">-DefaultProfile</span></span>
<span data-ttu-id="3bdc0-132">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bdc0-133">-Directory</span><span class="sxs-lookup"><span data-stu-id="3bdc0-133">-Directory</span></span>
<span data-ttu-id="3bdc0-134">Gibt einen Ordner als **CloudFileDirectory-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="3bdc0-135">Dieses Cmdlet erstellt den Ordner an dem Speicherort, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-135">This cmdlet creates the folder in the location that this parameter specifies.</span></span>
<span data-ttu-id="3bdc0-136">Verwenden Sie zum Abrufen eines Verzeichnisses das New-AzStorageDirectory Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-136">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="3bdc0-137">Sie können auch das cmdlet Get-AzStorageFile, um ein Verzeichnis zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-137">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3bdc0-138">-Path</span><span class="sxs-lookup"><span data-stu-id="3bdc0-138">-Path</span></span>
<span data-ttu-id="3bdc0-139">Gibt den Pfad eines Ordners an.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="3bdc0-140">Dieses Cmdlet erstellt einen Ordner für den Pfad, den dieses Cmdlet angibt.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-140">This cmdlet creates a folder for the path that this cmdlet specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3bdc0-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3bdc0-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3bdc0-142">Gibt die Länge des Auszeitzeitraums für den Serverteil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="3bdc0-143">-Teilen</span><span class="sxs-lookup"><span data-stu-id="3bdc0-143">-Share</span></span>
<span data-ttu-id="3bdc0-144">Gibt ein **CloudFileShare-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-144">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="3bdc0-145">Dieses Cmdlet erstellt einen Ordner in der Dateifreigabe, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-145">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>
<span data-ttu-id="3bdc0-146">Zum Abrufen eines **CloudFileShare-Objekts** verwenden Sie das Get-AzStorageShare Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-146">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="3bdc0-147">Dieses Objekt enthält den Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-147">This object contains the storage context.</span></span>
<span data-ttu-id="3bdc0-148">Wenn Sie diesen Parameter angeben, geben Sie den Parameter *Kontext nicht* an.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-148">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3bdc0-149">-ShareName</span><span class="sxs-lookup"><span data-stu-id="3bdc0-149">-ShareName</span></span>
<span data-ttu-id="3bdc0-150">Gibt den Namen der Dateifreigabe an.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-150">Specifies the name of the file share.</span></span>
<span data-ttu-id="3bdc0-151">Dieses Cmdlet erstellt einen Ordner in der Dateifreigabe, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-151">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bdc0-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bdc0-152">CommonParameters</span></span>
<span data-ttu-id="3bdc0-153">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bdc0-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bdc0-154">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bdc0-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bdc0-155">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3bdc0-155">INPUTS</span></span>

### <span data-ttu-id="3bdc0-156">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="3bdc0-156">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="3bdc0-157">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="3bdc0-157">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="3bdc0-158">System.String</span><span class="sxs-lookup"><span data-stu-id="3bdc0-158">System.String</span></span>

### <span data-ttu-id="3bdc0-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3bdc0-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3bdc0-160">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3bdc0-160">OUTPUTS</span></span>

### <span data-ttu-id="3bdc0-161">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileDirectory</span><span class="sxs-lookup"><span data-stu-id="3bdc0-161">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileDirectory</span></span>

## <span data-ttu-id="3bdc0-162">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3bdc0-162">NOTES</span></span>

## <span data-ttu-id="3bdc0-163">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3bdc0-163">RELATED LINKS</span></span>

[<span data-ttu-id="3bdc0-164">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="3bdc0-164">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="3bdc0-165">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="3bdc0-165">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="3bdc0-166">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="3bdc0-166">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="3bdc0-167">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="3bdc0-167">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="3bdc0-168">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="3bdc0-168">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)
