---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C1648DC3-8CFD-4487-A080-D9BE25DAD258
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
ms.openlocfilehash: b87c4169fb2a7d417f56051c4996cf0428ceafe7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165485"
---
# <span data-ttu-id="396a8-101">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="396a8-101">Get-AzStorageFileCopyState</span></span>

## <span data-ttu-id="396a8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="396a8-102">SYNOPSIS</span></span>
<span data-ttu-id="396a8-103">Ruft den Zustand eines Kopiervorgangs ab.</span><span class="sxs-lookup"><span data-stu-id="396a8-103">Gets the state of a copy operation.</span></span>

## <span data-ttu-id="396a8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="396a8-104">SYNTAX</span></span>

### <span data-ttu-id="396a8-105">ShareName</span><span class="sxs-lookup"><span data-stu-id="396a8-105">ShareName</span></span>
```
Get-AzStorageFileCopyState [-ShareName] <String> [-FilePath] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="396a8-106">Datei</span><span class="sxs-lookup"><span data-stu-id="396a8-106">File</span></span>
```
Get-AzStorageFileCopyState [-File] <CloudFile> [-WaitForComplete] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="396a8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="396a8-107">DESCRIPTION</span></span>
<span data-ttu-id="396a8-108">Das Cmdlet " **Get-AzStorageFileCopyState** " Ruft den Zustand eines Azure Storage-Dateikopiervorgangs ab.</span><span class="sxs-lookup"><span data-stu-id="396a8-108">The **Get-AzStorageFileCopyState** cmdlet gets the state of an Azure Storage file copy operation.</span></span>
<span data-ttu-id="396a8-109">Es sollte auf der Ziel Datei kopieren ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="396a8-109">It should run on the copy destination file.</span></span>

## <span data-ttu-id="396a8-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="396a8-110">EXAMPLES</span></span>

### <span data-ttu-id="396a8-111">Beispiel 1: Abrufen des Kopier Zustands nach dem Dateinamen</span><span class="sxs-lookup"><span data-stu-id="396a8-111">Example 1: Get the copy state by file name</span></span>
```
PS C:\>Get-AzStorageFileCopyState -ShareName "ContosoShare" -FilePath "ContosoFile"
```

<span data-ttu-id="396a8-112">Dieser Befehl ruft den Zustand des Kopiervorgangs für eine Datei ab, die den angegebenen Namen aufweist.</span><span class="sxs-lookup"><span data-stu-id="396a8-112">This command gets the state of the copy operation for a file that has the specified name.</span></span>

### <span data-ttu-id="396a8-113">Beispiel 2: Starten von "Kopieren und Pipeline", um den Kopierstatus zu erhalten</span><span class="sxs-lookup"><span data-stu-id="396a8-113">Example 2: Start Copy and pipeline to get the copy status</span></span>
```
C:\PS> $destfile = Start-AzStorageFileCopy -SrcShareName "contososhare" -SrcFilePath "contosofile" -DestShareName "contososhare2" -destfilepath "contosofile_copy"  

C:\PS> $destfile | Get-AzStorageFileCopyState
```

<span data-ttu-id="396a8-114">Mit dem ersten Befehl wird die Datei "contosodatei" in "contosofile_copy" kopiert, und das destiantion-Dateiobjekt wird ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="396a8-114">The first command starts copy file "contosofile" to "contosofile_copy", and output the destiantion file object.</span></span> <span data-ttu-id="396a8-115">Der zweite Befehl Pipeline das destiantion-Dateiobjekt zu Get-AzStorageFileCopyState, um den Datei Kopier Zustand abzurufen.</span><span class="sxs-lookup"><span data-stu-id="396a8-115">The second command pipeline the destiantion file object to Get-AzStorageFileCopyState, to get file copy state.</span></span>

## <span data-ttu-id="396a8-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="396a8-116">PARAMETERS</span></span>

### <span data-ttu-id="396a8-117">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="396a8-117">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="396a8-118">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="396a8-118">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="396a8-119">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="396a8-119">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="396a8-120">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="396a8-120">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="396a8-121">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="396a8-121">-ConcurrentTaskCount</span></span>
<span data-ttu-id="396a8-122">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="396a8-122">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="396a8-123">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="396a8-123">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="396a8-124">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="396a8-124">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="396a8-125">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="396a8-125">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="396a8-126">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="396a8-126">The default value is 10.</span></span>

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

### <span data-ttu-id="396a8-127">-Context</span><span class="sxs-lookup"><span data-stu-id="396a8-127">-Context</span></span>
<span data-ttu-id="396a8-128">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="396a8-128">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="396a8-129">Verwenden Sie zum Abrufen eines Kontexts das Cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="396a8-129">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="396a8-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="396a8-130">-DefaultProfile</span></span>
<span data-ttu-id="396a8-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="396a8-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="396a8-132">-Datei</span><span class="sxs-lookup"><span data-stu-id="396a8-132">-File</span></span>
<span data-ttu-id="396a8-133">Gibt ein **clouddatei** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="396a8-133">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="396a8-134">Mithilfe des Get-AzStorageFile-Cmdlets können Sie eine clouddatei erstellen oder eine Cloud-Datei abrufen.</span><span class="sxs-lookup"><span data-stu-id="396a8-134">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="396a8-135">-FilePath</span><span class="sxs-lookup"><span data-stu-id="396a8-135">-FilePath</span></span>
<span data-ttu-id="396a8-136">Gibt den Pfad der Datei relativ zu einer Azure-Speicherfreigabe an.</span><span class="sxs-lookup"><span data-stu-id="396a8-136">Specifies the path of the file relative to an Azure Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="396a8-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="396a8-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="396a8-138">Gibt die Länge des Timeoutzeitraums für den Server Teil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="396a8-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="396a8-139">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="396a8-139">-ShareName</span></span>
<span data-ttu-id="396a8-140">Gibt den Namen einer Freigabe an.</span><span class="sxs-lookup"><span data-stu-id="396a8-140">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="396a8-141">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="396a8-141">-WaitForComplete</span></span>
<span data-ttu-id="396a8-142">Gibt an, dass das Cmdlet auf die Fertigstellung der Kopie wartet.</span><span class="sxs-lookup"><span data-stu-id="396a8-142">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="396a8-143">Wenn Sie diesen Parameter nicht angeben, gibt dieses Cmdlet sofort ein Ergebnis zurück.</span><span class="sxs-lookup"><span data-stu-id="396a8-143">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="396a8-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="396a8-144">CommonParameters</span></span>
<span data-ttu-id="396a8-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="396a8-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="396a8-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="396a8-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="396a8-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="396a8-147">INPUTS</span></span>

### <span data-ttu-id="396a8-148">Microsoft. Azure. Storage. File. clouddatei</span><span class="sxs-lookup"><span data-stu-id="396a8-148">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="396a8-149">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="396a8-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="396a8-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="396a8-150">OUTPUTS</span></span>

### <span data-ttu-id="396a8-151">Microsoft. Azure. Storage. File. CopyState</span><span class="sxs-lookup"><span data-stu-id="396a8-151">Microsoft.Azure.Storage.File.CopyState</span></span>

## <span data-ttu-id="396a8-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="396a8-152">NOTES</span></span>

## <span data-ttu-id="396a8-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="396a8-153">RELATED LINKS</span></span>

[<span data-ttu-id="396a8-154">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="396a8-154">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="396a8-155">Neu – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="396a8-155">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="396a8-156">Anfang-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="396a8-156">Start-AzStorageFileCopy</span></span>](./Start-AzStorageFileCopy.md)

[<span data-ttu-id="396a8-157">Stopp-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="396a8-157">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)
