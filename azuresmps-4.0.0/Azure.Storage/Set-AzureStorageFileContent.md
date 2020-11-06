---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FA98E64B-D589-4653-9ACC-86573FAF4550
online version: ''
schema: 2.0.0
ms.openlocfilehash: bd066a57ac63b0126120652750c669e6afde36bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93474974"
---
# <span data-ttu-id="d5fb9-101">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d5fb9-101">Set-AzureStorageFileContent</span></span>

## <span data-ttu-id="d5fb9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d5fb9-102">SYNOPSIS</span></span>
<span data-ttu-id="d5fb9-103">Lädt den Inhalt einer Datei hoch.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-103">Uploads the contents of a file.</span></span>

## <span data-ttu-id="d5fb9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5fb9-104">SYNTAX</span></span>

### <span data-ttu-id="d5fb9-105">Freigabename (Standard)</span><span class="sxs-lookup"><span data-stu-id="d5fb9-105">ShareName (Default)</span></span>
```
Set-AzureStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5fb9-106">Freigeben</span><span class="sxs-lookup"><span data-stu-id="d5fb9-106">Share</span></span>
```
Set-AzureStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5fb9-107">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="d5fb9-107">Directory</span></span>
```
Set-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5fb9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d5fb9-108">DESCRIPTION</span></span>
<span data-ttu-id="d5fb9-109">Das Cmdlet " **Satz-AzureStorageFileContent** " lädt den Inhalt einer Datei in eine Datei auf einer bestimmten Freigabe hoch.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-109">The **Set-AzureStorageFileContent** cmdlet uploads the contents of a file to a file on a specified share.</span></span>

## <span data-ttu-id="d5fb9-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d5fb9-110">EXAMPLES</span></span>

### <span data-ttu-id="d5fb9-111">Beispiel 1: Hochladen einer Datei im aktuellen Ordner</span><span class="sxs-lookup"><span data-stu-id="d5fb9-111">Example 1: Upload a file in the current folder</span></span>
```
PS C:\>Set-AzureStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="d5fb9-112">Mit diesem Befehl wird eine Datei mit dem Namen DataFile37 im aktuellen Ordner als Datei mit dem Namen CurrentDataFile im Ordner "ContosoWorkingFolder" hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-112">This command uploads a file that is named DataFile37 in the current folder as a file that is named CurrentDataFile in the folder named ContosoWorkingFolder.</span></span>

### <span data-ttu-id="d5fb9-113">Beispiel 2: Hochladen aller Dateien im aktuellen Ordner</span><span class="sxs-lookup"><span data-stu-id="d5fb9-113">Example 2: Upload all the files in the current folder</span></span>
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzureStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzureStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

<span data-ttu-id="d5fb9-114">In diesem Beispiel werden mehrere allgemeine Windows PowerShell-Cmdlets und das aktuelle Cmdlet verwendet, um alle Dateien aus dem aktuellen Ordner in den Stammordner des Container-ContosoShare06 hochzuladen.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-114">This example uses several common Windows PowerShell cmdlets and the current cmdlet to upload all files from the current folder to the root folder of container ContosoShare06.</span></span>

<span data-ttu-id="d5fb9-115">Der erste Befehl ruft den Namen des aktuellen Ordners ab und speichert ihn in der $CurrentFolder-Variablen.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-115">The first command gets the name of the current folder and stores it in the $CurrentFolder variable.</span></span>

<span data-ttu-id="d5fb9-116">Der zweite Befehl verwendet das Cmdlet " **Get-AzureStorageShare** ", um die Dateifreigabe mit dem Namen ContosoShare06 abzurufen, und speichert Sie dann in der $Container-Variablen.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-116">The second command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="d5fb9-117">Der endgültige Befehl ruft den Inhalt des aktuellen Ordners ab und übergibt ihn mithilfe des Pipelineoperators an das Where-Object-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-117">The final command gets the contents of the current folder and passes each one to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d5fb9-118">Dieses Cmdlet filtert Objekte, die keine Dateien sind, und übergibt die Dateien an das ForEach-Object-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-118">That cmdlet filters out objects that are not files, and then passes the files to the ForEach-Object cmdlet.</span></span>
<span data-ttu-id="d5fb9-119">Dieses Cmdlet führt einen Skriptblock für jede Datei aus, die den entsprechenden Pfad dafür erstellt, und verwendet dann das aktuelle Cmdlet, um die Datei hochzuladen.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-119">That cmdlet runs a script block for each file that creates the appropriate path for it and then uses the current cmdlet to upload the file.</span></span>
<span data-ttu-id="d5fb9-120">Das Ergebnis hat denselben Namen und dieselbe relative Position hinsichtlich der anderen Dateien, die in diesem Beispiel hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-120">The result has the same name and same relative position with regard to the other files that this example uploads.</span></span>
<span data-ttu-id="d5fb9-121">Wenn Sie weitere Informationen zu Skriptblöcken wünschen, geben Sie `Get-Help about_Script_Blocks` .</span><span class="sxs-lookup"><span data-stu-id="d5fb9-121">For more information about script blocks, type `Get-Help about_Script_Blocks`.</span></span>

## <span data-ttu-id="d5fb9-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5fb9-122">PARAMETERS</span></span>

### <span data-ttu-id="d5fb9-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d5fb9-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d5fb9-124">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d5fb9-125">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d5fb9-126">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d5fb9-127">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d5fb9-127">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d5fb9-128">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-128">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="d5fb9-129">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-129">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="d5fb9-130">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-130">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="d5fb9-131">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-131">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="d5fb9-132">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-132">The default value is 10.</span></span>

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

### <span data-ttu-id="d5fb9-133">-Context</span><span class="sxs-lookup"><span data-stu-id="d5fb9-133">-Context</span></span>
<span data-ttu-id="d5fb9-134">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-134">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d5fb9-135">Verwenden Sie zum Abrufen eines Speicher Kontexts das Cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="d5fb9-135">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5fb9-136">-Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="d5fb9-136">-Directory</span></span>
<span data-ttu-id="d5fb9-137">Gibt einen Ordner als **CloudFileDirectory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-137">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="d5fb9-138">Mit diesem Cmdlet wird die Datei in den Ordner hochgeladen, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-138">This cmdlet uploads the file to the folder that this parameter specifies.</span></span>
<span data-ttu-id="d5fb9-139">Verwenden Sie das New-AzureStorageDirectory-Cmdlet, um ein Verzeichnis zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-139">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="d5fb9-140">Sie können auch das Get-AzureStorageFile-Cmdlet verwenden, um ein Verzeichnis abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-140">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: CloudFileDirectory
Parameter Sets: Directory
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5fb9-141">-Force</span><span class="sxs-lookup"><span data-stu-id="d5fb9-141">-Force</span></span>
<span data-ttu-id="d5fb9-142">Gibt an, dass mit diesem Cmdlet eine vorhandene Azure-Speicherdatei überschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-142">Indicates that this cmdlet overwrites an existing Azure storage file.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5fb9-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d5fb9-143">-PassThru</span></span>
<span data-ttu-id="d5fb9-144">Gibt an, dass dieses Cmdlet das **AzureStorageFile** -Objekt zurückgibt, das erstellt oder hochgeladen wird.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-144">Indicates that this cmdlet returns the **AzureStorageFile** object that it creates or uploads.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5fb9-145">-Path</span><span class="sxs-lookup"><span data-stu-id="d5fb9-145">-Path</span></span>
<span data-ttu-id="d5fb9-146">Gibt den Pfad einer Datei oder eines Ordners an.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-146">Specifies the path of a file or folder.</span></span>
<span data-ttu-id="d5fb9-147">Mit diesem Cmdlet wird der Inhalt in die Datei hochgeladen, die dieser Parameter angibt, oder auf eine Datei im Ordner, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-147">This cmdlet uploads contents to the file that this parameter specifies, or to a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="d5fb9-148">Wenn Sie einen Ordner angeben, wird mit diesem Cmdlet eine Datei erstellt, die den gleichen Namen wie die Quelldatei aufweist.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-148">If you specify a folder, this cmdlet creates a file that has the same name as the source file.</span></span>

<span data-ttu-id="d5fb9-149">Wenn Sie einen Pfad einer Datei angeben, die nicht vorhanden ist, erstellt dieses Cmdlet diese Datei und speichert die Inhalte in dieser Datei.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-149">If you specify a path of a file that does not exist, this cmdlet creates that file and saves the contents to that file.</span></span>
<span data-ttu-id="d5fb9-150">Wenn Sie eine Datei angeben, die bereits vorhanden ist, und Sie den Parameter _Force_ angeben, wird der Inhalt der Datei von diesem Cmdlet überschrieben.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-150">If you specify a file that already exists, and you specify the _Force_ parameter, this cmdlet overwrites the contents of the file.</span></span>
<span data-ttu-id="d5fb9-151">Wenn Sie eine Datei angeben, die bereits vorhanden ist, und Sie _Force_ nicht angeben, gibt dieses Cmdlet keine Änderungen und gibt einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-151">If you specify a file that already exists and you do not specify _Force_ , this cmdlet makes no change, and returns an error.</span></span>

<span data-ttu-id="d5fb9-152">Wenn Sie einen Pfad eines Ordners angeben, der nicht vorhanden ist, nimmt dieses Cmdlet keine Änderungen vor und gibt einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-152">If you specify a path of a folder that does not exist, this cmdlet makes no change, and returns an error.</span></span>


```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5fb9-153">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d5fb9-153">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d5fb9-154">Gibt die Länge des Timeoutzeitraums für den Server Teil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-154">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="d5fb9-155">-Freigeben</span><span class="sxs-lookup"><span data-stu-id="d5fb9-155">-Share</span></span>
<span data-ttu-id="d5fb9-156">Gibt ein **CloudFileShare** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-156">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="d5fb9-157">Dieses Cmdlet wird in eine Datei in der Dateifreigabe, die dieser Parameter angibt, hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-157">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>
<span data-ttu-id="d5fb9-158">Verwenden Sie das Get-AzureStorageShare-Cmdlet, um ein **CloudFileShare** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-158">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="d5fb9-159">Dieses Objekt enthält den Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-159">This object contains the storage context.</span></span>
<span data-ttu-id="d5fb9-160">Wenn Sie diesen Parameter angeben, geben Sie den *context* -Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-160">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5fb9-161">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="d5fb9-161">-ShareName</span></span>
<span data-ttu-id="d5fb9-162">Gibt den Namen der Dateifreigabe an.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-162">Specifies the name of the file share.</span></span>
<span data-ttu-id="d5fb9-163">Dieses Cmdlet wird in eine Datei in der Dateifreigabe, die dieser Parameter angibt, hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-163">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5fb9-164">-Source</span><span class="sxs-lookup"><span data-stu-id="d5fb9-164">-Source</span></span>
<span data-ttu-id="d5fb9-165">Gibt die Quelldatei an, die von diesem Cmdlet hochgeladen wird.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-165">Specifies the source file that this cmdlet uploads.</span></span>
<span data-ttu-id="d5fb9-166">Wenn Sie eine Datei angeben, die nicht vorhanden ist, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-166">If you specify a file that does not exist, this cmdlet returns an error.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: FullName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5fb9-167">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d5fb9-167">-Confirm</span></span>
<span data-ttu-id="d5fb9-168">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-168">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5fb9-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5fb9-169">-WhatIf</span></span>
<span data-ttu-id="d5fb9-170">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5fb9-171">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-171">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5fb9-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5fb9-172">CommonParameters</span></span>
<span data-ttu-id="d5fb9-173">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5fb9-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5fb9-174">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5fb9-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5fb9-175">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d5fb9-175">INPUTS</span></span>

## <span data-ttu-id="d5fb9-176">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d5fb9-176">OUTPUTS</span></span>

## <span data-ttu-id="d5fb9-177">Notizen</span><span class="sxs-lookup"><span data-stu-id="d5fb9-177">NOTES</span></span>

## <span data-ttu-id="d5fb9-178">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d5fb9-178">RELATED LINKS</span></span>

[<span data-ttu-id="d5fb9-179">Remove-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="d5fb9-179">Remove-AzureStorageDirectory</span></span>](./Remove-AzureStorageDirectory.md)

[<span data-ttu-id="d5fb9-180">Neu – AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="d5fb9-180">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)

[<span data-ttu-id="d5fb9-181">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d5fb9-181">Get-AzureStorageFileContent</span></span>](./Get-AzureStorageFileContent.md)
