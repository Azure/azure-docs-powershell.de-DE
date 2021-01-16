---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3AC3F8DE-E25D-41AE-9083-5C459A4C8CD0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/stop-azstoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageFileCopy.md
ms.openlocfilehash: ac36914167bd5bda2e79576d9879d6f8c92ba7fd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376003"
---
# <span data-ttu-id="d2e1e-101">Stop-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="d2e1e-101">Stop-AzStorageFileCopy</span></span>

## <span data-ttu-id="d2e1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2e1e-102">SYNOPSIS</span></span>
<span data-ttu-id="d2e1e-103">Beendet einen Kopiervorgang in die angegebene Zieldatei.</span><span class="sxs-lookup"><span data-stu-id="d2e1e-103">Stops a copy operation to the specified destination file.</span></span>

## <span data-ttu-id="d2e1e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d2e1e-104">SYNTAX</span></span>

### <span data-ttu-id="d2e1e-105">ShareName</span><span class="sxs-lookup"><span data-stu-id="d2e1e-105">ShareName</span></span>
```
Stop-AzStorageFileCopy [-ShareName] <String> [-FilePath] <String> [-CopyId <String>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d2e1e-106">Datei</span><span class="sxs-lookup"><span data-stu-id="d2e1e-106">File</span></span>
```
Stop-AzStorageFileCopy [-File] <CloudFile> [-CopyId <String>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2e1e-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d2e1e-107">DESCRIPTION</span></span>
<span data-ttu-id="d2e1e-108">Das **Cmdlet "Stop-AzStorageFileCopy"** beendet das Kopieren einer Datei in eine Zieldatei.</span><span class="sxs-lookup"><span data-stu-id="d2e1e-108">The **Stop-AzStorageFileCopy** cmdlet stops copying a file to a destination file.</span></span>

## <span data-ttu-id="d2e1e-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d2e1e-109">EXAMPLES</span></span>

### <span data-ttu-id="d2e1e-110">Beispiel 1: Beenden eines Kopiervorgangs</span><span class="sxs-lookup"><span data-stu-id="d2e1e-110">Example 1: Stop a copy operation</span></span>
```
PS C:\>Stop-AzStorageFileCopy -ShareName "ContosoShare" -FilePath "FilePath" -CopyId "CopyId"
```

<span data-ttu-id="d2e1e-111">Dieser Befehl beendet das Kopieren einer Datei mit dem angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="d2e1e-111">This command stops copying a file that has the specified name.</span></span>

## <span data-ttu-id="d2e1e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2e1e-112">PARAMETERS</span></span>

### <span data-ttu-id="d2e1e-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d2e1e-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d2e1e-114">Gibt das clientseitige Zeitintervall (in Sekunden) für eine Serviceanfrage an.</span><span class="sxs-lookup"><span data-stu-id="d2e1e-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d2e1e-115">Wenn der vorherige Aufruf im angegebenen Intervall fehlschlägt, wird die Anforderung von diesem Cmdlet erneut ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d2e1e-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d2e1e-116">Wenn dieses Cmdlet vor Ablauf des Intervalls keine erfolgreiche Antwort erhält, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="d2e1e-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d2e1e-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d2e1e-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d2e1e-118">Gibt die maximalen gleichzeitigen Netzwerkanrufe an.</span><span class="sxs-lookup"><span data-stu-id="d2e1e-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="d2e1e-119">Sie können diesen Parameter verwenden, um die Parallelität zum Drosseln der lokalen CPU- und Bandbreitenverwendung zu beschränken, indem Sie die maximale Anzahl gleichzeitiger Netzwerkaufrufe angeben.</span><span class="sxs-lookup"><span data-stu-id="d2e1e-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="d2e1e-120">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der Anzahl der Kernwerte multipliziert.</span><span class="sxs-lookup"><span data-stu-id="d2e1e-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="d2e1e-121">Dieser Parameter kann zur Verringerung von Netzwerkverbindungsproblemen in Umgebungen mit geringer Bandbreite beitragen, z. B. 100 Kilobit pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="d2e1e-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="d2e1e-122">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="d2e1e-122">The default value is 10.</span></span>

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

### <span data-ttu-id="d2e1e-123">-Context</span><span class="sxs-lookup"><span data-stu-id="d2e1e-123">-Context</span></span>
<span data-ttu-id="d2e1e-124">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="d2e1e-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="d2e1e-125">Verwenden Sie zum Abrufen eines Speicherkontexts das [Cmdlet "New-AzStorageContext".](./New-AzStorageContext.md)</span><span class="sxs-lookup"><span data-stu-id="d2e1e-125">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="d2e1e-126">-CopyId</span><span class="sxs-lookup"><span data-stu-id="d2e1e-126">-CopyId</span></span>
<span data-ttu-id="d2e1e-127">Gibt die ID des Kopiervorgangs an.</span><span class="sxs-lookup"><span data-stu-id="d2e1e-127">Specifies the ID of the copy operation.</span></span>

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

### <span data-ttu-id="d2e1e-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2e1e-128">-DefaultProfile</span></span>
<span data-ttu-id="d2e1e-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d2e1e-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2e1e-130">-File</span><span class="sxs-lookup"><span data-stu-id="d2e1e-130">-File</span></span>
<span data-ttu-id="d2e1e-131">Gibt ein **CloudFile-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="d2e1e-131">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="d2e1e-132">Sie können eine Clouddatei erstellen oder sie mithilfe des cmdlets Get-AzStorageFile abrufen.</span><span class="sxs-lookup"><span data-stu-id="d2e1e-132">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="d2e1e-133">-FilePath</span><span class="sxs-lookup"><span data-stu-id="d2e1e-133">-FilePath</span></span>
<span data-ttu-id="d2e1e-134">Gibt den Pfad einer Datei an.</span><span class="sxs-lookup"><span data-stu-id="d2e1e-134">Specifies the path of a file.</span></span>

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

### <span data-ttu-id="d2e1e-135">-Force</span><span class="sxs-lookup"><span data-stu-id="d2e1e-135">-Force</span></span>
<span data-ttu-id="d2e1e-136">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="d2e1e-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d2e1e-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d2e1e-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d2e1e-138">Gibt die Länge des Zeitzeitraums für den Serverteil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="d2e1e-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="d2e1e-139">-ShareName</span><span class="sxs-lookup"><span data-stu-id="d2e1e-139">-ShareName</span></span>
<span data-ttu-id="d2e1e-140">Gibt den Namen einer Freigabe an.</span><span class="sxs-lookup"><span data-stu-id="d2e1e-140">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="d2e1e-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2e1e-141">-Confirm</span></span>
<span data-ttu-id="d2e1e-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d2e1e-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2e1e-143">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d2e1e-143">-WhatIf</span></span>
<span data-ttu-id="d2e1e-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d2e1e-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2e1e-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d2e1e-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2e1e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2e1e-146">CommonParameters</span></span>
<span data-ttu-id="d2e1e-147">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2e1e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2e1e-148">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2e1e-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2e1e-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d2e1e-149">INPUTS</span></span>

### <span data-ttu-id="d2e1e-150">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="d2e1e-150">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="d2e1e-151">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d2e1e-151">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d2e1e-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d2e1e-152">OUTPUTS</span></span>

### <span data-ttu-id="d2e1e-153">System.Void</span><span class="sxs-lookup"><span data-stu-id="d2e1e-153">System.Void</span></span>

## <span data-ttu-id="d2e1e-154">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d2e1e-154">NOTES</span></span>

## <span data-ttu-id="d2e1e-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d2e1e-155">RELATED LINKS</span></span>

[<span data-ttu-id="d2e1e-156">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="d2e1e-156">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="d2e1e-157">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="d2e1e-157">Get-AzStorageFileCopyState</span></span>](./Get-AzStorageFileCopyState.md)

[<span data-ttu-id="d2e1e-158">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="d2e1e-158">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="d2e1e-159">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="d2e1e-159">Start-AzStorageFileCopy</span></span>](./Start-AzStorageFileCopy.md)
