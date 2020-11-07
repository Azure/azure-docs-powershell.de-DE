---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 65962F9A-CC79-4B8B-9208-A993708FD36F
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragedirectory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageDirectory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageDirectory.md
ms.openlocfilehash: 5965ef718a24a428dab84ddab8dc07495e2d8662
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823908"
---
# <span data-ttu-id="46d3d-101">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="46d3d-101">New-AzStorageDirectory</span></span>

## <span data-ttu-id="46d3d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="46d3d-102">SYNOPSIS</span></span>
<span data-ttu-id="46d3d-103">Erstellt ein Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="46d3d-103">Creates a directory.</span></span>

## <span data-ttu-id="46d3d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="46d3d-104">SYNTAX</span></span>

### <span data-ttu-id="46d3d-105">Freigabename (Standard)</span><span class="sxs-lookup"><span data-stu-id="46d3d-105">ShareName (Default)</span></span>
```
New-AzStorageDirectory [-ShareName] <String> [-Path] <String> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="46d3d-106">Freigeben</span><span class="sxs-lookup"><span data-stu-id="46d3d-106">Share</span></span>
```
New-AzStorageDirectory [-Share] <CloudFileShare> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="46d3d-107">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="46d3d-107">Directory</span></span>
```
New-AzStorageDirectory [-Directory] <CloudFileDirectory> [-Path] <String> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="46d3d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46d3d-108">DESCRIPTION</span></span>
<span data-ttu-id="46d3d-109">Das Cmdlet **New-AzStorageDirectory** erstellt ein Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="46d3d-109">The **New-AzStorageDirectory** cmdlet creates a directory.</span></span>
<span data-ttu-id="46d3d-110">Dieses Cmdlet gibt ein **CloudFileDirectory** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="46d3d-110">This cmdlet returns a **CloudFileDirectory** object.</span></span>

## <span data-ttu-id="46d3d-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="46d3d-111">EXAMPLES</span></span>

### <span data-ttu-id="46d3d-112">Beispiel 1: Erstellen eines Ordners in einer Dateifreigabe</span><span class="sxs-lookup"><span data-stu-id="46d3d-112">Example 1: Create a folder in a file share</span></span>
```
PS C:\>New-AzStorageDirectory -ShareName "ContosoShare06" -Path "ContosoWorkingFolder"
```

<span data-ttu-id="46d3d-113">Dieser Befehl erstellt einen Ordner mit dem Namen ContosoWorkingFolder in der Dateifreigabe mit dem Namen ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="46d3d-113">This command creates a folder named ContosoWorkingFolder in the file share named ContosoShare06.</span></span>

### <span data-ttu-id="46d3d-114">Beispiel 2: Erstellen eines Ordners in einer Dateifreigabe, die in einem Dateifreigabe Objekt angegeben ist</span><span class="sxs-lookup"><span data-stu-id="46d3d-114">Example 2: Create a folder in a file share specified in a file share object</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" | New-AzStorageDirectory -Path "ContosoWorkingFolder"
```

<span data-ttu-id="46d3d-115">Dieser Befehl verwendet das Cmdlet " **Get-AzStorageShare** ", um die Dateifreigabe mit dem Namen ContosoShare06 abzurufen, und übergibt Sie dann mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46d3d-115">This command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="46d3d-116">Das aktuelle Cmdlet erstellt den Ordner mit dem Namen ContosoWorkingFolder in ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="46d3d-116">The current cmdlet creates the folder named ContosoWorkingFolder in ContosoShare06.</span></span>

## <span data-ttu-id="46d3d-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="46d3d-117">PARAMETERS</span></span>

### <span data-ttu-id="46d3d-118">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="46d3d-118">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="46d3d-119">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="46d3d-119">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="46d3d-120">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="46d3d-120">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="46d3d-121">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="46d3d-121">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="46d3d-122">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="46d3d-122">-ConcurrentTaskCount</span></span>
<span data-ttu-id="46d3d-123">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="46d3d-123">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="46d3d-124">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="46d3d-124">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="46d3d-125">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="46d3d-125">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="46d3d-126">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="46d3d-126">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="46d3d-127">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="46d3d-127">The default value is 10.</span></span>

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

### <span data-ttu-id="46d3d-128">-Context</span><span class="sxs-lookup"><span data-stu-id="46d3d-128">-Context</span></span>
<span data-ttu-id="46d3d-129">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="46d3d-129">Specifies an Azure storage context.</span></span>
<span data-ttu-id="46d3d-130">Verwenden Sie zum Abrufen eines Speicher Kontexts das Cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="46d3d-130">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="46d3d-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46d3d-131">-DefaultProfile</span></span>
<span data-ttu-id="46d3d-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="46d3d-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46d3d-133">-Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="46d3d-133">-Directory</span></span>
<span data-ttu-id="46d3d-134">Gibt einen Ordner als **CloudFileDirectory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="46d3d-134">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="46d3d-135">Mit diesem Cmdlet wird der Ordner an dem Speicherort erstellt, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="46d3d-135">This cmdlet creates the folder in the location that this parameter specifies.</span></span>
<span data-ttu-id="46d3d-136">Verwenden Sie das New-AzStorageDirectory-Cmdlet, um ein Verzeichnis zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="46d3d-136">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="46d3d-137">Sie können auch das Get-AzStorageFile-Cmdlet verwenden, um ein Verzeichnis abzurufen.</span><span class="sxs-lookup"><span data-stu-id="46d3d-137">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46d3d-138">-Path</span><span class="sxs-lookup"><span data-stu-id="46d3d-138">-Path</span></span>
<span data-ttu-id="46d3d-139">Gibt den Pfad eines Ordners an.</span><span class="sxs-lookup"><span data-stu-id="46d3d-139">Specifies the path of a folder.</span></span>
<span data-ttu-id="46d3d-140">Dieses Cmdlet erstellt einen Ordner für den von diesem Cmdlet festgelegten Pfad.</span><span class="sxs-lookup"><span data-stu-id="46d3d-140">This cmdlet creates a folder for the path that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="46d3d-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="46d3d-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="46d3d-142">Gibt die Länge des Timeoutzeitraums für den Server Teil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="46d3d-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="46d3d-143">-Freigeben</span><span class="sxs-lookup"><span data-stu-id="46d3d-143">-Share</span></span>
<span data-ttu-id="46d3d-144">Gibt ein **CloudFileShare** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="46d3d-144">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="46d3d-145">Dieses Cmdlet erstellt einen Ordner in der Dateifreigabe, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="46d3d-145">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>
<span data-ttu-id="46d3d-146">Verwenden Sie das Get-AzStorageShare-Cmdlet, um ein **CloudFileShare** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="46d3d-146">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="46d3d-147">Dieses Objekt enthält den Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="46d3d-147">This object contains the storage context.</span></span>
<span data-ttu-id="46d3d-148">Wenn Sie diesen Parameter angeben, geben Sie den *context* -Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="46d3d-148">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46d3d-149">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="46d3d-149">-ShareName</span></span>
<span data-ttu-id="46d3d-150">Gibt den Namen der Dateifreigabe an.</span><span class="sxs-lookup"><span data-stu-id="46d3d-150">Specifies the name of the file share.</span></span>
<span data-ttu-id="46d3d-151">Dieses Cmdlet erstellt einen Ordner in der Dateifreigabe, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="46d3d-151">This cmdlet creates a folder in the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="46d3d-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46d3d-152">CommonParameters</span></span>
<span data-ttu-id="46d3d-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46d3d-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46d3d-154">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46d3d-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46d3d-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="46d3d-155">INPUTS</span></span>

### <span data-ttu-id="46d3d-156">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="46d3d-156">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="46d3d-157">Microsoft. Azure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="46d3d-157">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="46d3d-158">System. String</span><span class="sxs-lookup"><span data-stu-id="46d3d-158">System.String</span></span>

### <span data-ttu-id="46d3d-159">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="46d3d-159">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="46d3d-160">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="46d3d-160">OUTPUTS</span></span>

### <span data-ttu-id="46d3d-161">Microsoft. Azure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="46d3d-161">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

## <span data-ttu-id="46d3d-162">Notizen</span><span class="sxs-lookup"><span data-stu-id="46d3d-162">NOTES</span></span>

## <span data-ttu-id="46d3d-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="46d3d-163">RELATED LINKS</span></span>

[<span data-ttu-id="46d3d-164">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="46d3d-164">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="46d3d-165">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="46d3d-165">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="46d3d-166">Neu – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="46d3d-166">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="46d3d-167">Neu – AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="46d3d-167">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="46d3d-168">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="46d3d-168">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)
