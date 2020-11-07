---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3AC3F8DE-E25D-41AE-9083-5C459A4C8CD0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/stop-azstoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Stop-AzStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Stop-AzStorageFileCopy.md
ms.openlocfilehash: ce00ee3fa67477bfdced040fb8c990ff11dc4504
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842824"
---
# <span data-ttu-id="faca5-101">Stop-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="faca5-101">Stop-AzStorageFileCopy</span></span>

## <span data-ttu-id="faca5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="faca5-102">SYNOPSIS</span></span>
<span data-ttu-id="faca5-103">Beendet einen Kopiervorgang in der angegebenen Zieldatei.</span><span class="sxs-lookup"><span data-stu-id="faca5-103">Stops a copy operation to the specified destination file.</span></span>

## <span data-ttu-id="faca5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="faca5-104">SYNTAX</span></span>

### <span data-ttu-id="faca5-105">ShareName</span><span class="sxs-lookup"><span data-stu-id="faca5-105">ShareName</span></span>
```
Stop-AzStorageFileCopy [-ShareName] <String> [-FilePath] <String> [-CopyId <String>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="faca5-106">Datei</span><span class="sxs-lookup"><span data-stu-id="faca5-106">File</span></span>
```
Stop-AzStorageFileCopy [-File] <CloudFile> [-CopyId <String>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="faca5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="faca5-107">DESCRIPTION</span></span>
<span data-ttu-id="faca5-108">Das Cmdlet **Stop-AzStorageFileCopy** beendet das Kopieren einer Datei in eine Zieldatei.</span><span class="sxs-lookup"><span data-stu-id="faca5-108">The **Stop-AzStorageFileCopy** cmdlet stops copying a file to a destination file.</span></span>

## <span data-ttu-id="faca5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="faca5-109">EXAMPLES</span></span>

### <span data-ttu-id="faca5-110">Beispiel 1: Beenden eines Kopiervorgangs</span><span class="sxs-lookup"><span data-stu-id="faca5-110">Example 1: Stop a copy operation</span></span>
```
PS C:\>Stop-AzStorageFileCopy -ShareName "ContosoShare" -FilePath "FilePath" -CopyId "CopyId"
```

<span data-ttu-id="faca5-111">Dieser Befehl beendet das Kopieren einer Datei mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="faca5-111">This command stops copying a file that has the specified name.</span></span>

## <span data-ttu-id="faca5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="faca5-112">PARAMETERS</span></span>

### <span data-ttu-id="faca5-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="faca5-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="faca5-114">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="faca5-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="faca5-115">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="faca5-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="faca5-116">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="faca5-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="faca5-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="faca5-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="faca5-118">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="faca5-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="faca5-119">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="faca5-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="faca5-120">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="faca5-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="faca5-121">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="faca5-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="faca5-122">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="faca5-122">The default value is 10.</span></span>

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

### <span data-ttu-id="faca5-123">-Context</span><span class="sxs-lookup"><span data-stu-id="faca5-123">-Context</span></span>
<span data-ttu-id="faca5-124">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="faca5-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="faca5-125">Verwenden Sie zum Abrufen eines Speicher Kontexts das Cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="faca5-125">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="faca5-126">-Kopier-Nr</span><span class="sxs-lookup"><span data-stu-id="faca5-126">-CopyId</span></span>
<span data-ttu-id="faca5-127">Gibt die ID des Kopiervorgangs an.</span><span class="sxs-lookup"><span data-stu-id="faca5-127">Specifies the ID of the copy operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faca5-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faca5-128">-DefaultProfile</span></span>
<span data-ttu-id="faca5-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="faca5-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="faca5-130">-Datei</span><span class="sxs-lookup"><span data-stu-id="faca5-130">-File</span></span>
<span data-ttu-id="faca5-131">Gibt ein **clouddatei** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="faca5-131">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="faca5-132">Mithilfe des Get-AzStorageFile-Cmdlets können Sie eine clouddatei erstellen oder eine Cloud-Datei abrufen.</span><span class="sxs-lookup"><span data-stu-id="faca5-132">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="faca5-133">-FilePath</span><span class="sxs-lookup"><span data-stu-id="faca5-133">-FilePath</span></span>
<span data-ttu-id="faca5-134">Gibt den Pfad einer Datei an.</span><span class="sxs-lookup"><span data-stu-id="faca5-134">Specifies the path of a file.</span></span>

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

### <span data-ttu-id="faca5-135">-Force</span><span class="sxs-lookup"><span data-stu-id="faca5-135">-Force</span></span>
<span data-ttu-id="faca5-136">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="faca5-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="faca5-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="faca5-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="faca5-138">Gibt die Länge des Timeoutzeitraums für den Server Teil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="faca5-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="faca5-139">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="faca5-139">-ShareName</span></span>
<span data-ttu-id="faca5-140">Gibt den Namen einer Freigabe an.</span><span class="sxs-lookup"><span data-stu-id="faca5-140">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="faca5-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="faca5-141">-Confirm</span></span>
<span data-ttu-id="faca5-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="faca5-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="faca5-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="faca5-143">-WhatIf</span></span>
<span data-ttu-id="faca5-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="faca5-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="faca5-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="faca5-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="faca5-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faca5-146">CommonParameters</span></span>
<span data-ttu-id="faca5-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="faca5-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faca5-148">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="faca5-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faca5-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="faca5-149">INPUTS</span></span>

### <span data-ttu-id="faca5-150">Microsoft. WindowsAz. Storage. File. clouddatei</span><span class="sxs-lookup"><span data-stu-id="faca5-150">Microsoft.WindowsAz.Storage.File.CloudFile</span></span>
<span data-ttu-id="faca5-151">Parameter: Datei (ByValue)</span><span class="sxs-lookup"><span data-stu-id="faca5-151">Parameters: File (ByValue)</span></span>

### <span data-ttu-id="faca5-152">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="faca5-152">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="faca5-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="faca5-153">OUTPUTS</span></span>

### <span data-ttu-id="faca5-154">System. void</span><span class="sxs-lookup"><span data-stu-id="faca5-154">System.Void</span></span>

## <span data-ttu-id="faca5-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="faca5-155">NOTES</span></span>

## <span data-ttu-id="faca5-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="faca5-156">RELATED LINKS</span></span>

[<span data-ttu-id="faca5-157">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="faca5-157">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="faca5-158">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="faca5-158">Get-AzStorageFileCopyState</span></span>](./Get-AzStorageFileCopyState.md)

[<span data-ttu-id="faca5-159">Neu – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="faca5-159">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="faca5-160">Anfang-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="faca5-160">Start-AzStorageFileCopy</span></span>](./Start-AzStorageFileCopy.md)
