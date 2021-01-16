---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FA98E64B-D589-4653-9ACC-86573FAF4550
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
ms.openlocfilehash: 3fed30a260532378274e2df815d6e4b252c018f6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376142"
---
# <span data-ttu-id="9e3aa-101">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="9e3aa-101">Set-AzStorageFileContent</span></span>

## <span data-ttu-id="9e3aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e3aa-102">SYNOPSIS</span></span>
<span data-ttu-id="9e3aa-103">Lädt den Inhalt einer Datei hoch.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-103">Uploads the contents of a file.</span></span>

## <span data-ttu-id="9e3aa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9e3aa-104">SYNTAX</span></span>

### <span data-ttu-id="9e3aa-105">ShareName (Standard)</span><span class="sxs-lookup"><span data-stu-id="9e3aa-105">ShareName (Default)</span></span>
```
Set-AzStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="9e3aa-106">Freigeben</span><span class="sxs-lookup"><span data-stu-id="9e3aa-106">Share</span></span>
```
Set-AzStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="9e3aa-107">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="9e3aa-107">Directory</span></span>
```
Set-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## <span data-ttu-id="9e3aa-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9e3aa-108">DESCRIPTION</span></span>
<span data-ttu-id="9e3aa-109">Das **Cmdlet Set-AzStorageFileContent** lädt den Inhalt einer Datei in eine Datei auf einer angegebenen Freigabe hoch.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-109">The **Set-AzStorageFileContent** cmdlet uploads the contents of a file to a file on a specified share.</span></span>

## <span data-ttu-id="9e3aa-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9e3aa-110">EXAMPLES</span></span>

### <span data-ttu-id="9e3aa-111">Beispiel 1: Hochladen einer Datei im aktuellen Ordner</span><span class="sxs-lookup"><span data-stu-id="9e3aa-111">Example 1: Upload a file in the current folder</span></span>
```
PS C:\>Set-AzStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="9e3aa-112">Mit diesem Befehl wird eine Datei mit dem Namen "DataFile37" im aktuellen Ordner als Datei mit dem Namen "CurrentDataFile" im Ordner "ContosoWorkingFolder" hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-112">This command uploads a file that is named DataFile37 in the current folder as a file that is named CurrentDataFile in the folder named ContosoWorkingFolder.</span></span>

### <span data-ttu-id="9e3aa-113">Beispiel 2: Hochladen aller Dateien im aktuellen Ordner</span><span class="sxs-lookup"><span data-stu-id="9e3aa-113">Example 2: Upload all the files in the current folder</span></span>
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

<span data-ttu-id="9e3aa-114">In diesem Beispiel werden mehrere Windows PowerShell cmdlets und das aktuelle Cmdlet verwendet, um alle Dateien aus dem aktuellen Ordner in den Stammordner des Container "ContosoShare06" hochzuladen.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-114">This example uses several common Windows PowerShell cmdlets and the current cmdlet to upload all files from the current folder to the root folder of container ContosoShare06.</span></span>
<span data-ttu-id="9e3aa-115">Der erste Befehl ruft den Namen des aktuellen Ordners ab und speichert ihn in der $CurrentFolder Variable.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-115">The first command gets the name of the current folder and stores it in the $CurrentFolder variable.</span></span>
<span data-ttu-id="9e3aa-116">Der zweite Befehl verwendet das **Cmdlet "Get-AzStorageShare",** um die Dateifreigabe namens "ContosoShare06" zu erhalten, und speichert sie dann in der $Container Variable.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-116">The second command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="9e3aa-117">Der letzte Befehl ruft den Inhalt des aktuellen Ordners ab und übergibt jeden mit dem Pipelineoperator Where-Object an das cmdlet "Where-Object".</span><span class="sxs-lookup"><span data-stu-id="9e3aa-117">The final command gets the contents of the current folder and passes each one to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9e3aa-118">Dieses Cmdlet filtert Objekte heraus, die keine Dateien sind, und übergibt die Dateien dann an ForEach-Object Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-118">That cmdlet filters out objects that are not files, and then passes the files to the ForEach-Object cmdlet.</span></span>
<span data-ttu-id="9e3aa-119">Dieses Cmdlet führt einen Skriptblock für jede Datei aus, die den entsprechenden Pfad dafür erstellt und dann das aktuelle Cmdlet zum Hochladen der Datei verwendet.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-119">That cmdlet runs a script block for each file that creates the appropriate path for it and then uses the current cmdlet to upload the file.</span></span>
<span data-ttu-id="9e3aa-120">Das Ergebnis hat denselben Namen und dieselbe relative Position in Bezug auf die anderen Dateien, die in diesem Beispiel hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-120">The result has the same name and same relative position with regard to the other files that this example uploads.</span></span>
<span data-ttu-id="9e3aa-121">Geben Sie weitere Informationen zu Skriptblöcken `Get-Help about_Script_Blocks` ein.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-121">For more information about script blocks, type `Get-Help about_Script_Blocks`.</span></span>

### <span data-ttu-id="9e3aa-122">Beispiel 3: Laden Sie eine lokale Datei in eine Azure-Datei hoch, und reservieren Sie die lokalen Datei-SMB-Eigenschaften (File Attributtes, File Creation Time, File Last Write Time) in der Azure-Datei.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-122">Example 3: Upload a local file to an Azure file, and perserve the local File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the Azure file.</span></span>
```
PS C:\>Get-AzStorageFileContent -source $localFilePath -ShareName sample -Path "dir1/file1" -PreserveSMBAttribute
```

<span data-ttu-id="9e3aa-123">In diesem Beispiel wird eine lokale Datei in eine Azure-Datei hochgeladen, und die lokalen Datei-SMB-Eigenschaften (File Attributtes, File Creation Time, File Last Write Time) in der Azure-Datei werden gespeichert.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-123">This example uploads a local file to an Azure file, and perserves the local File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the Azure file.</span></span>

## <span data-ttu-id="9e3aa-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e3aa-124">PARAMETERS</span></span>

### <span data-ttu-id="9e3aa-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e3aa-125">-AsJob</span></span>
<span data-ttu-id="9e3aa-126">Führen Sie das Cmdlet im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-126">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="9e3aa-127">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9e3aa-127">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9e3aa-128">Gibt das clientseitige Zeitintervall (in Sekunden) für eine Serviceanfrage an.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-128">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9e3aa-129">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-129">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9e3aa-130">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-130">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9e3aa-131">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9e3aa-131">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9e3aa-132">Gibt die maximalen gleichzeitigen Netzwerkanrufe an.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-132">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="9e3aa-133">Sie können diesen Parameter verwenden, um die Parallelität zur Einschränkung der lokalen CPU- und Bandbreitennutzung zu beschränken, indem Sie die maximale Anzahl von gleichzeitigen Netzwerkaufrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-133">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="9e3aa-134">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Anzahl der Kernwerte multipliziert.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-134">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="9e3aa-135">Dieser Parameter kann zur Verringerung von Netzwerkverbindungsproblemen in Umgebungen mit geringer Bandbreite beitragen, z. B. 100 Kilobit pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-135">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="9e3aa-136">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-136">The default value is 10.</span></span>

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

### <span data-ttu-id="9e3aa-137">-Context</span><span class="sxs-lookup"><span data-stu-id="9e3aa-137">-Context</span></span>
<span data-ttu-id="9e3aa-138">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-138">Specifies an Azure storage context.</span></span>
<span data-ttu-id="9e3aa-139">Verwenden Sie zum Abrufen eines Speicherkontexts das [Cmdlet "New-AzStorageContext".](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="9e3aa-139">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="9e3aa-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e3aa-140">-DefaultProfile</span></span>
<span data-ttu-id="9e3aa-141">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e3aa-142">-Directory</span><span class="sxs-lookup"><span data-stu-id="9e3aa-142">-Directory</span></span>
<span data-ttu-id="9e3aa-143">Gibt einen Ordner als **CloudFileDirectory-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-143">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="9e3aa-144">Dieses Cmdlet lädt die Datei in den Ordner hoch, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-144">This cmdlet uploads the file to the folder that this parameter specifies.</span></span>
<span data-ttu-id="9e3aa-145">Verwenden Sie zum Abrufen eines Verzeichnisses das New-AzStorageDirectory Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-145">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="9e3aa-146">Sie können auch das Get-AzStorageFile zum Abrufen eines Verzeichnisses verwenden.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-146">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="9e3aa-147">-Force</span><span class="sxs-lookup"><span data-stu-id="9e3aa-147">-Force</span></span>
<span data-ttu-id="9e3aa-148">Gibt an, dass dieses Cmdlet eine vorhandene Azure -Speicherdatei überschreibt.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-148">Indicates that this cmdlet overwrites an existing Azure storage file.</span></span>

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

### <span data-ttu-id="9e3aa-149">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e3aa-149">-PassThru</span></span>
<span data-ttu-id="9e3aa-150">Gibt an, dass dieses Cmdlet das **azureStorageFile-Objekt** zurückgibt, das erstellt oder hochgeladen wird.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-150">Indicates that this cmdlet returns the **AzureStorageFile** object that it creates or uploads.</span></span>

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

### <span data-ttu-id="9e3aa-151">-Path</span><span class="sxs-lookup"><span data-stu-id="9e3aa-151">-Path</span></span>
<span data-ttu-id="9e3aa-152">Gibt den Pfad einer Datei oder eines Ordners an.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-152">Specifies the path of a file or folder.</span></span>
<span data-ttu-id="9e3aa-153">Dieses Cmdlet lädt Inhalte in die Datei hoch, die dieser Parameter angibt, oder in eine Datei in dem Ordner, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-153">This cmdlet uploads contents to the file that this parameter specifies, or to a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="9e3aa-154">Wenn Sie einen Ordner angeben, erstellt dieses Cmdlet eine Datei mit demselben Namen wie die Quelldatei.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-154">If you specify a folder, this cmdlet creates a file that has the same name as the source file.</span></span>
<span data-ttu-id="9e3aa-155">Wenn Sie einen Pfad für eine Datei angeben, die nicht vorhanden ist, erstellt dieses Cmdlet diese Datei und speichert den Inhalt in dieser Datei.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-155">If you specify a path of a file that does not exist, this cmdlet creates that file and saves the contents to that file.</span></span>
<span data-ttu-id="9e3aa-156">Wenn Sie eine Datei angeben, die bereits vorhanden ist, und den Parameter _"Erzwingen"_ angeben, überschreibt dieses Cmdlet den Inhalt der Datei.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-156">If you specify a file that already exists, and you specify the _Force_ parameter, this cmdlet overwrites the contents of the file.</span></span>
<span data-ttu-id="9e3aa-157">Wenn Sie eine Datei angeben, die bereits vorhanden ist, aber nicht "Erzwingen" _angeben,_ nimmt dieses Cmdlet keine Änderung vor und gibt einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-157">If you specify a file that already exists and you do not specify _Force_, this cmdlet makes no change, and returns an error.</span></span>
<span data-ttu-id="9e3aa-158">Wenn Sie einen Pfad eines Ordners angeben, der nicht vorhanden ist, nimmt dieses Cmdlet keine Änderung vor und gibt einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-158">If you specify a path of a folder that does not exist, this cmdlet makes no change, and returns an error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e3aa-159">-PreserveSMBAttribute</span><span class="sxs-lookup"><span data-stu-id="9e3aa-159">-PreserveSMBAttribute</span></span>
<span data-ttu-id="9e3aa-160">Behalten Sie die Eigenschaften des Quelldatei-SMB (File Attributtes, File Creation Time, File Last Write Time) in der Zieldatei bei.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-160">Keep the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in destination File.</span></span> <span data-ttu-id="9e3aa-161">Dieser Parameter ist nur unter Windows verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-161">This parameter is only available on Windows.</span></span>

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

### <span data-ttu-id="9e3aa-162">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9e3aa-162">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9e3aa-163">Gibt die Länge des Zeitzeitraums für den Serverteil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-163">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="9e3aa-164">-Teilen</span><span class="sxs-lookup"><span data-stu-id="9e3aa-164">-Share</span></span>
<span data-ttu-id="9e3aa-165">Gibt ein **CloudFileShare-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-165">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="9e3aa-166">Dieses Cmdlet lädt in eine Datei in der Dateifreigabe hoch, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-166">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>
<span data-ttu-id="9e3aa-167">Verwenden Sie zum Abrufen **eines CloudFileShare-Objekts** das Get-AzStorageShare Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-167">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="9e3aa-168">Dieses Objekt enthält den Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-168">This object contains the storage context.</span></span>
<span data-ttu-id="9e3aa-169">Wenn Sie diesen Parameter angeben, geben Sie den *Kontextparameter nicht* an.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-169">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="9e3aa-170">-ShareName</span><span class="sxs-lookup"><span data-stu-id="9e3aa-170">-ShareName</span></span>
<span data-ttu-id="9e3aa-171">Gibt den Namen der Dateifreigabe an.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-171">Specifies the name of the file share.</span></span>
<span data-ttu-id="9e3aa-172">Dieses Cmdlet lädt in eine Datei in der Dateifreigabe hoch, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-172">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>

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

### <span data-ttu-id="9e3aa-173">-Source</span><span class="sxs-lookup"><span data-stu-id="9e3aa-173">-Source</span></span>
<span data-ttu-id="9e3aa-174">Gibt die Quelldatei an, die von diesem Cmdlet hochgeladen wird.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-174">Specifies the source file that this cmdlet uploads.</span></span>
<span data-ttu-id="9e3aa-175">Wenn Sie eine Datei angeben, die nicht vorhanden ist, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-175">If you specify a file that does not exist, this cmdlet returns an error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FullName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e3aa-176">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9e3aa-176">-Confirm</span></span>
<span data-ttu-id="9e3aa-177">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-177">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e3aa-178">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="9e3aa-178">-WhatIf</span></span>
<span data-ttu-id="9e3aa-179">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e3aa-180">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-180">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e3aa-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e3aa-181">CommonParameters</span></span>
<span data-ttu-id="9e3aa-182">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e3aa-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e3aa-183">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e3aa-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e3aa-184">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9e3aa-184">INPUTS</span></span>

### <span data-ttu-id="9e3aa-185">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="9e3aa-185">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="9e3aa-186">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="9e3aa-186">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="9e3aa-187">System.String</span><span class="sxs-lookup"><span data-stu-id="9e3aa-187">System.String</span></span>

### <span data-ttu-id="9e3aa-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9e3aa-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9e3aa-189">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9e3aa-189">OUTPUTS</span></span>

### <span data-ttu-id="9e3aa-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="9e3aa-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="9e3aa-191">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9e3aa-191">NOTES</span></span>

## <span data-ttu-id="9e3aa-192">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9e3aa-192">RELATED LINKS</span></span>

[<span data-ttu-id="9e3aa-193">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="9e3aa-193">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)

[<span data-ttu-id="9e3aa-194">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="9e3aa-194">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="9e3aa-195">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="9e3aa-195">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)
