---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C1648DC3-8CFD-4487-A080-D9BE25DAD258
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
ms.openlocfilehash: b87c4169fb2a7d417f56051c4996cf0428ceafe7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458208"
---
# <span data-ttu-id="9b3ef-101">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="9b3ef-101">Get-AzStorageFileCopyState</span></span>

## <span data-ttu-id="9b3ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b3ef-102">SYNOPSIS</span></span>
<span data-ttu-id="9b3ef-103">Ruft den Zustand eines Kopiervorgangs ab.</span><span class="sxs-lookup"><span data-stu-id="9b3ef-103">Gets the state of a copy operation.</span></span>

## <span data-ttu-id="9b3ef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9b3ef-104">SYNTAX</span></span>

### <span data-ttu-id="9b3ef-105">ShareName</span><span class="sxs-lookup"><span data-stu-id="9b3ef-105">ShareName</span></span>
```
Get-AzStorageFileCopyState [-ShareName] <String> [-FilePath] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="9b3ef-106">Datei</span><span class="sxs-lookup"><span data-stu-id="9b3ef-106">File</span></span>
```
Get-AzStorageFileCopyState [-File] <CloudFile> [-WaitForComplete] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="9b3ef-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9b3ef-107">DESCRIPTION</span></span>
<span data-ttu-id="9b3ef-108">Das **Cmdlet "Get-AzStorageFileCopyState"** ruft den Zustand eines Kopiervorgangs für eine Azure Storage-Datei ab.</span><span class="sxs-lookup"><span data-stu-id="9b3ef-108">The **Get-AzStorageFileCopyState** cmdlet gets the state of an Azure Storage file copy operation.</span></span>
<span data-ttu-id="9b3ef-109">Sie sollte für die Zieldatei zum Kopieren ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9b3ef-109">It should run on the copy destination file.</span></span>

## <span data-ttu-id="9b3ef-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9b3ef-110">EXAMPLES</span></span>

### <span data-ttu-id="9b3ef-111">Beispiel 1: Herunterladen des Kopierstatus nach Dateiname</span><span class="sxs-lookup"><span data-stu-id="9b3ef-111">Example 1: Get the copy state by file name</span></span>
```
PS C:\>Get-AzStorageFileCopyState -ShareName "ContosoShare" -FilePath "ContosoFile"
```

<span data-ttu-id="9b3ef-112">Dieser Befehl ruft den Zustand des Kopiervorgangs für eine Datei mit dem angegebenen Namen ab.</span><span class="sxs-lookup"><span data-stu-id="9b3ef-112">This command gets the state of the copy operation for a file that has the specified name.</span></span>

### <span data-ttu-id="9b3ef-113">Beispiel 2: Starten von "Kopieren und Pipeline", um den Kopierstatus zu erhalten</span><span class="sxs-lookup"><span data-stu-id="9b3ef-113">Example 2: Start Copy and pipeline to get the copy status</span></span>
```
C:\PS> $destfile = Start-AzStorageFileCopy -SrcShareName "contososhare" -SrcFilePath "contosofile" -DestShareName "contososhare2" -destfilepath "contosofile_copy"  

C:\PS> $destfile | Get-AzStorageFileCopyState
```

<span data-ttu-id="9b3ef-114">Der erste Befehl startet das Kopieren der Datei "contosofile" in "contosofile_copy", und gibt das Destlikationsdateiobjekt aus.</span><span class="sxs-lookup"><span data-stu-id="9b3ef-114">The first command starts copy file "contosofile" to "contosofile_copy", and output the destiantion file object.</span></span> <span data-ttu-id="9b3ef-115">Die zweite Befehlspipeline des Deslikationsdateiobjekts zu "Get-AzStorageFileCopyState", um den Dateikopiezustand zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9b3ef-115">The second command pipeline the destiantion file object to Get-AzStorageFileCopyState, to get file copy state.</span></span>

## <span data-ttu-id="9b3ef-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b3ef-116">PARAMETERS</span></span>

### <span data-ttu-id="9b3ef-117">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9b3ef-117">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9b3ef-118">Gibt das clientseitige Zeitintervall (in Sekunden) für eine Serviceanfrage an.</span><span class="sxs-lookup"><span data-stu-id="9b3ef-118">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9b3ef-119">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9b3ef-119">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9b3ef-120">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="9b3ef-120">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9b3ef-121">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9b3ef-121">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9b3ef-122">Gibt die maximalen gleichzeitigen Netzwerkanrufe an.</span><span class="sxs-lookup"><span data-stu-id="9b3ef-122">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="9b3ef-123">Sie können diesen Parameter verwenden, um die Parallelität zum Drosseln der lokalen CPU- und Bandbreitenverwendung zu beschränken, indem Sie die maximale Anzahl gleichzeitiger Netzwerkaufrufe angeben.</span><span class="sxs-lookup"><span data-stu-id="9b3ef-123">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="9b3ef-124">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Anzahl der Kernwerte multipliziert.</span><span class="sxs-lookup"><span data-stu-id="9b3ef-124">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="9b3ef-125">Dieser Parameter kann zur Verringerung von Netzwerkverbindungsproblemen in Umgebungen mit geringer Bandbreite beitragen, z. B. 100 Kilobit pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="9b3ef-125">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="9b3ef-126">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="9b3ef-126">The default value is 10.</span></span>

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

### <span data-ttu-id="9b3ef-127">-Context</span><span class="sxs-lookup"><span data-stu-id="9b3ef-127">-Context</span></span>
<span data-ttu-id="9b3ef-128">Gibt einen Azure Storage-Kontext an.</span><span class="sxs-lookup"><span data-stu-id="9b3ef-128">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="9b3ef-129">Verwenden Sie zum Abrufen eines Kontexts das [Cmdlet "New-AzStorageContext".](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="9b3ef-129">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="9b3ef-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b3ef-130">-DefaultProfile</span></span>
<span data-ttu-id="9b3ef-131">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9b3ef-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b3ef-132">-File</span><span class="sxs-lookup"><span data-stu-id="9b3ef-132">-File</span></span>
<span data-ttu-id="9b3ef-133">Gibt ein **CloudFile-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="9b3ef-133">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="9b3ef-134">Sie können eine Clouddatei erstellen oder sie mithilfe des cmdlets Get-AzStorageFile abrufen.</span><span class="sxs-lookup"><span data-stu-id="9b3ef-134">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="9b3ef-135">-FilePath</span><span class="sxs-lookup"><span data-stu-id="9b3ef-135">-FilePath</span></span>
<span data-ttu-id="9b3ef-136">Gibt den Pfad der Datei relativ zu einer Azure Storage Share an.</span><span class="sxs-lookup"><span data-stu-id="9b3ef-136">Specifies the path of the file relative to an Azure Storage share.</span></span>

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

### <span data-ttu-id="9b3ef-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9b3ef-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9b3ef-138">Gibt die Länge des Zeitzeitraums für den Serverteil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="9b3ef-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="9b3ef-139">-ShareName</span><span class="sxs-lookup"><span data-stu-id="9b3ef-139">-ShareName</span></span>
<span data-ttu-id="9b3ef-140">Gibt den Namen einer Freigabe an.</span><span class="sxs-lookup"><span data-stu-id="9b3ef-140">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="9b3ef-141">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="9b3ef-141">-WaitForComplete</span></span>
<span data-ttu-id="9b3ef-142">Zeigt an, dass dieses Cmdlet auf den Abschluss der Kopie wartet.</span><span class="sxs-lookup"><span data-stu-id="9b3ef-142">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="9b3ef-143">Wenn Sie diesen Parameter nicht angeben, gibt dieses Cmdlet sofort ein Ergebnis zurück.</span><span class="sxs-lookup"><span data-stu-id="9b3ef-143">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="9b3ef-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b3ef-144">CommonParameters</span></span>
<span data-ttu-id="9b3ef-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b3ef-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b3ef-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b3ef-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b3ef-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9b3ef-147">INPUTS</span></span>

### <span data-ttu-id="9b3ef-148">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="9b3ef-148">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="9b3ef-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9b3ef-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9b3ef-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9b3ef-150">OUTPUTS</span></span>

### <span data-ttu-id="9b3ef-151">Microsoft.Azure.Storage.File.CopyState</span><span class="sxs-lookup"><span data-stu-id="9b3ef-151">Microsoft.Azure.Storage.File.CopyState</span></span>

## <span data-ttu-id="9b3ef-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9b3ef-152">NOTES</span></span>

## <span data-ttu-id="9b3ef-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9b3ef-153">RELATED LINKS</span></span>

[<span data-ttu-id="9b3ef-154">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="9b3ef-154">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="9b3ef-155">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="9b3ef-155">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="9b3ef-156">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="9b3ef-156">Start-AzStorageFileCopy</span></span>](./Start-AzStorageFileCopy.md)

[<span data-ttu-id="9b3ef-157">Stop-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="9b3ef-157">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)
