---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 3AC3F8DE-E25D-41AE-9083-5C459A4C8CD0
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/stop-azurestoragefilecopy
schema: 2.0.0
ms.openlocfilehash: c0db10c24f019a9f91efd4ad9ec6805ffc3b0208
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848344"
---
# <span data-ttu-id="937c7-101">Stop-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="937c7-101">Stop-AzureStorageFileCopy</span></span>

## <span data-ttu-id="937c7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="937c7-102">SYNOPSIS</span></span>
<span data-ttu-id="937c7-103">Beendet einen Kopiervorgang in der angegebenen Zieldatei.</span><span class="sxs-lookup"><span data-stu-id="937c7-103">Stops a copy operation to the specified destination file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="937c7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="937c7-104">SYNTAX</span></span>

### <span data-ttu-id="937c7-105">ShareName</span><span class="sxs-lookup"><span data-stu-id="937c7-105">ShareName</span></span>
```
Stop-AzureStorageFileCopy [-ShareName] <String> [-FilePath] <String> [-CopyId <String>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="937c7-106">Datei</span><span class="sxs-lookup"><span data-stu-id="937c7-106">File</span></span>
```
Stop-AzureStorageFileCopy [-File] <CloudFile> [-CopyId <String>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="937c7-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="937c7-107">DESCRIPTION</span></span>
<span data-ttu-id="937c7-108">Das Cmdlet **Stop-AzureStorageFileCopy** beendet das Kopieren einer Datei in eine Zieldatei.</span><span class="sxs-lookup"><span data-stu-id="937c7-108">The **Stop-AzureStorageFileCopy** cmdlet stops copying a file to a destination file.</span></span>

## <span data-ttu-id="937c7-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="937c7-109">EXAMPLES</span></span>

### <span data-ttu-id="937c7-110">Beispiel 1: Beenden eines Kopiervorgangs</span><span class="sxs-lookup"><span data-stu-id="937c7-110">Example 1: Stop a copy operation</span></span>
```
PS C:\>Stop-AzureStorageFileCopy -ShareName "ContosoShare" -FilePath "FilePath" -CopyId "CopyId"
```

<span data-ttu-id="937c7-111">Dieser Befehl beendet das Kopieren einer Datei mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="937c7-111">This command stops copying a file that has the specified name.</span></span>

## <span data-ttu-id="937c7-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="937c7-112">PARAMETERS</span></span>

### <span data-ttu-id="937c7-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="937c7-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="937c7-114">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="937c7-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="937c7-115">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="937c7-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="937c7-116">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="937c7-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="937c7-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="937c7-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="937c7-118">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="937c7-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="937c7-119">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="937c7-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="937c7-120">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="937c7-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="937c7-121">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="937c7-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="937c7-122">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="937c7-122">The default value is 10.</span></span>

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

### <span data-ttu-id="937c7-123">-Context</span><span class="sxs-lookup"><span data-stu-id="937c7-123">-Context</span></span>
<span data-ttu-id="937c7-124">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="937c7-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="937c7-125">Verwenden Sie zum Abrufen eines Speicher Kontexts das Cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="937c7-125">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="937c7-126">-Kopier-Nr</span><span class="sxs-lookup"><span data-stu-id="937c7-126">-CopyId</span></span>
<span data-ttu-id="937c7-127">Gibt die ID des Kopiervorgangs an.</span><span class="sxs-lookup"><span data-stu-id="937c7-127">Specifies the ID of the copy operation.</span></span>

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

### <span data-ttu-id="937c7-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="937c7-128">-DefaultProfile</span></span>
<span data-ttu-id="937c7-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="937c7-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="937c7-130">-Datei</span><span class="sxs-lookup"><span data-stu-id="937c7-130">-File</span></span>
<span data-ttu-id="937c7-131">Gibt ein **clouddatei** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="937c7-131">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="937c7-132">Mithilfe des Get-AzureStorageFile-Cmdlets können Sie eine clouddatei erstellen oder eine Cloud-Datei abrufen.</span><span class="sxs-lookup"><span data-stu-id="937c7-132">You can create a cloud file or obtain one by using the Get-AzureStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="937c7-133">-FilePath</span><span class="sxs-lookup"><span data-stu-id="937c7-133">-FilePath</span></span>
<span data-ttu-id="937c7-134">Gibt den Pfad einer Datei an.</span><span class="sxs-lookup"><span data-stu-id="937c7-134">Specifies the path of a file.</span></span>

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

### <span data-ttu-id="937c7-135">-Force</span><span class="sxs-lookup"><span data-stu-id="937c7-135">-Force</span></span>
<span data-ttu-id="937c7-136">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="937c7-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="937c7-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="937c7-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="937c7-138">Gibt die Länge des Timeoutzeitraums für den Server Teil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="937c7-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="937c7-139">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="937c7-139">-ShareName</span></span>
<span data-ttu-id="937c7-140">Gibt den Namen einer Freigabe an.</span><span class="sxs-lookup"><span data-stu-id="937c7-140">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="937c7-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="937c7-141">-Confirm</span></span>
<span data-ttu-id="937c7-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="937c7-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="937c7-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="937c7-143">-WhatIf</span></span>
<span data-ttu-id="937c7-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="937c7-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="937c7-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="937c7-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="937c7-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="937c7-146">CommonParameters</span></span>
<span data-ttu-id="937c7-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="937c7-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="937c7-148">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="937c7-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="937c7-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="937c7-149">INPUTS</span></span>

### <span data-ttu-id="937c7-150">Microsoft. WindowsAzure. Storage. File. clouddatei</span><span class="sxs-lookup"><span data-stu-id="937c7-150">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>
<span data-ttu-id="937c7-151">Parameter: Datei (ByValue)</span><span class="sxs-lookup"><span data-stu-id="937c7-151">Parameters: File (ByValue)</span></span>

### <span data-ttu-id="937c7-152">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="937c7-152">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="937c7-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="937c7-153">OUTPUTS</span></span>

### <span data-ttu-id="937c7-154">System. void</span><span class="sxs-lookup"><span data-stu-id="937c7-154">System.Void</span></span>

## <span data-ttu-id="937c7-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="937c7-155">NOTES</span></span>

## <span data-ttu-id="937c7-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="937c7-156">RELATED LINKS</span></span>

[<span data-ttu-id="937c7-157">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="937c7-157">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="937c7-158">Get-AzureStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="937c7-158">Get-AzureStorageFileCopyState</span></span>](./Get-AzureStorageFileCopyState.md)

[<span data-ttu-id="937c7-159">Neu – AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="937c7-159">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="937c7-160">Anfang-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="937c7-160">Start-AzureStorageFileCopy</span></span>](./Start-AzureStorageFileCopy.md)
