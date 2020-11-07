---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C1648DC3-8CFD-4487-A080-D9BE25DAD258
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileCopyState.md
ms.openlocfilehash: 84d4abf2e06cf647e3674bcded88211ab727f8c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826580"
---
# <span data-ttu-id="49a41-101">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="49a41-101">Get-AzStorageFileCopyState</span></span>

## <span data-ttu-id="49a41-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="49a41-102">SYNOPSIS</span></span>
<span data-ttu-id="49a41-103">Ruft den Zustand eines Kopiervorgangs ab.</span><span class="sxs-lookup"><span data-stu-id="49a41-103">Gets the state of a copy operation.</span></span>

## <span data-ttu-id="49a41-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="49a41-104">SYNTAX</span></span>

### <span data-ttu-id="49a41-105">ShareName</span><span class="sxs-lookup"><span data-stu-id="49a41-105">ShareName</span></span>
```
Get-AzStorageFileCopyState [-ShareName] <String> [-FilePath] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="49a41-106">Datei</span><span class="sxs-lookup"><span data-stu-id="49a41-106">File</span></span>
```
Get-AzStorageFileCopyState [-File] <CloudFile> [-WaitForComplete] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="49a41-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="49a41-107">DESCRIPTION</span></span>
<span data-ttu-id="49a41-108">Das Cmdlet " **Get-AzStorageFileCopyState** " Ruft den Zustand eines Azure Storage-Dateikopiervorgangs ab.</span><span class="sxs-lookup"><span data-stu-id="49a41-108">The **Get-AzStorageFileCopyState** cmdlet gets the state of an Azure Storage file copy operation.</span></span>

## <span data-ttu-id="49a41-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="49a41-109">EXAMPLES</span></span>

### <span data-ttu-id="49a41-110">Beispiel 1: Abrufen des Kopier Zustands nach dem Dateinamen</span><span class="sxs-lookup"><span data-stu-id="49a41-110">Example 1: Get the copy state by file name</span></span>
```
PS C:\>Get-AzStorageFileCopyState -ShareName "ContosoShare" -FilePath "ContosoFile"
```

<span data-ttu-id="49a41-111">Dieser Befehl ruft den Zustand des Kopiervorgangs für eine Datei ab, die den angegebenen Namen aufweist.</span><span class="sxs-lookup"><span data-stu-id="49a41-111">This command gets the state of the copy operation for a file that has the specified name.</span></span>

## <span data-ttu-id="49a41-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="49a41-112">PARAMETERS</span></span>

### <span data-ttu-id="49a41-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="49a41-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="49a41-114">Gibt das clientseitige Timeoutintervall für eine Dienstanforderung in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="49a41-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="49a41-115">Wenn der vorherige Anruf im angegebenen Intervall fehlschlägt, versucht dieses Cmdlet die Anforderung erneut.</span><span class="sxs-lookup"><span data-stu-id="49a41-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="49a41-116">Wenn dieses Cmdlet keine erfolgreiche Antwort erhält, bevor das Intervall verstreicht, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="49a41-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="49a41-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="49a41-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="49a41-118">Gibt die maximale Anzahl gleichzeitiger Netzwerk Anrufe an.</span><span class="sxs-lookup"><span data-stu-id="49a41-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="49a41-119">Sie können diesen Parameter verwenden, um die Parallelität zu begrenzen, um die lokale CPU-und Bandbreitennutzung zu drosseln, indem Sie die maximale Anzahl von gleichzeitigen Netzwerk anrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="49a41-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="49a41-120">Der angegebene Wert ist eine absolute Anzahl und wird nicht mit der kernanzahl multipliziert.</span><span class="sxs-lookup"><span data-stu-id="49a41-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="49a41-121">Mithilfe dieses Parameters können Netzwerkverbindungsprobleme in Umgebungen mit niedriger Bandbreite wie 100 kbit/s verringert werden.</span><span class="sxs-lookup"><span data-stu-id="49a41-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="49a41-122">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="49a41-122">The default value is 10.</span></span>

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

### <span data-ttu-id="49a41-123">-Context</span><span class="sxs-lookup"><span data-stu-id="49a41-123">-Context</span></span>
<span data-ttu-id="49a41-124">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="49a41-124">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="49a41-125">Verwenden Sie zum Abrufen eines Kontexts das Cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="49a41-125">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="49a41-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49a41-126">-DefaultProfile</span></span>
<span data-ttu-id="49a41-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="49a41-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49a41-128">-Datei</span><span class="sxs-lookup"><span data-stu-id="49a41-128">-File</span></span>
<span data-ttu-id="49a41-129">Gibt ein **clouddatei** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="49a41-129">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="49a41-130">Mithilfe des Get-AzStorageFile-Cmdlets können Sie eine clouddatei erstellen oder eine Cloud-Datei abrufen.</span><span class="sxs-lookup"><span data-stu-id="49a41-130">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49a41-131">-FilePath</span><span class="sxs-lookup"><span data-stu-id="49a41-131">-FilePath</span></span>
<span data-ttu-id="49a41-132">Gibt den Pfad der Datei relativ zu einer Azure-Speicherfreigabe an.</span><span class="sxs-lookup"><span data-stu-id="49a41-132">Specifies the path of the file relative to an Azure Storage share.</span></span>

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

### <span data-ttu-id="49a41-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="49a41-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="49a41-134">Gibt die Länge des Timeoutzeitraums für den Server Teil einer Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="49a41-134">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="49a41-135">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="49a41-135">-ShareName</span></span>
<span data-ttu-id="49a41-136">Gibt den Namen einer Freigabe an.</span><span class="sxs-lookup"><span data-stu-id="49a41-136">Specifies the name of a share.</span></span>

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

### <span data-ttu-id="49a41-137">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="49a41-137">-WaitForComplete</span></span>
<span data-ttu-id="49a41-138">Gibt an, dass das Cmdlet auf die Fertigstellung der Kopie wartet.</span><span class="sxs-lookup"><span data-stu-id="49a41-138">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="49a41-139">Wenn Sie diesen Parameter nicht angeben, gibt dieses Cmdlet sofort ein Ergebnis zurück.</span><span class="sxs-lookup"><span data-stu-id="49a41-139">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="49a41-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49a41-140">CommonParameters</span></span>
<span data-ttu-id="49a41-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49a41-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49a41-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49a41-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49a41-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="49a41-143">INPUTS</span></span>

### <span data-ttu-id="49a41-144">Microsoft. Azure. Storage. File. clouddatei</span><span class="sxs-lookup"><span data-stu-id="49a41-144">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="49a41-145">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="49a41-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="49a41-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="49a41-146">OUTPUTS</span></span>

### <span data-ttu-id="49a41-147">Microsoft. Azure. Storage. File. clouddatei</span><span class="sxs-lookup"><span data-stu-id="49a41-147">Microsoft.Azure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="49a41-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="49a41-148">NOTES</span></span>

## <span data-ttu-id="49a41-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="49a41-149">RELATED LINKS</span></span>

[<span data-ttu-id="49a41-150">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="49a41-150">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="49a41-151">Neu – AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="49a41-151">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="49a41-152">Anfang-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="49a41-152">Start-AzStorageFileCopy</span></span>](./Start-AzStorageFileCopy.md)

[<span data-ttu-id="49a41-153">Stopp-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="49a41-153">Stop-AzStorageFileCopy</span></span>](./Stop-AzStorageFileCopy.md)
