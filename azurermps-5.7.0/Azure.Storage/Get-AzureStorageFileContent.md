---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFileContent.md
ms.openlocfilehash: 1dc1e95e2ecf085faad664f624e7595acd9ab607
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496777"
---
# <span data-ttu-id="fc19e-101">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="fc19e-101">Get-AzureStorageFileContent</span></span>

## <span data-ttu-id="fc19e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fc19e-102">SYNOPSIS</span></span>
<span data-ttu-id="fc19e-103">Lädt den Inhalt einer Datei herunter.</span><span class="sxs-lookup"><span data-stu-id="fc19e-103">Downloads the contents of a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc19e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fc19e-104">SYNTAX</span></span>

### <span data-ttu-id="fc19e-105">Freigabename (Standard)</span><span class="sxs-lookup"><span data-stu-id="fc19e-105">ShareName (Default)</span></span>
```
Get-AzureStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc19e-106">Freigeben</span><span class="sxs-lookup"><span data-stu-id="fc19e-106">Share</span></span>
```
Get-AzureStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc19e-107">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="fc19e-107">Directory</span></span>
```
Get-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc19e-108">Datei</span><span class="sxs-lookup"><span data-stu-id="fc19e-108">File</span></span>
```
Get-AzureStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc19e-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fc19e-109">DESCRIPTION</span></span>
<span data-ttu-id="fc19e-110">Das Cmdlet " **Get-AzureStorageFileContent** " downloadet den Inhalt einer Datei und speichert Sie dann in einem von Ihnen angegebenen Ziel.</span><span class="sxs-lookup"><span data-stu-id="fc19e-110">The **Get-AzureStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="fc19e-111">Dieses Cmdlet gibt nicht den Inhalt der Datei zurück.</span><span class="sxs-lookup"><span data-stu-id="fc19e-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="fc19e-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fc19e-112">EXAMPLES</span></span>

### <span data-ttu-id="fc19e-113">Beispiel 1: Herunterladen einer Datei aus einem Ordner</span><span class="sxs-lookup"><span data-stu-id="fc19e-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzureStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="fc19e-114">Dieser Befehl downloadet eine Datei mit dem Namen CurrentDataFile im Ordner ContosoWorkingFolder aus der Dateifreigabe ContosoShare06 in den aktuellen Ordner.</span><span class="sxs-lookup"><span data-stu-id="fc19e-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="fc19e-115">Beispiel 2: Herunterladen der Dateien unter Beispieldatei Freigabe</span><span class="sxs-lookup"><span data-stu-id="fc19e-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzureStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzureStorageFileContent
```

<span data-ttu-id="fc19e-116">In diesem Beispiel werden die Dateien unter Beispieldatei Freigabe heruntergeladen</span><span class="sxs-lookup"><span data-stu-id="fc19e-116">This example downloads the files under sample file share</span></span>

## <span data-ttu-id="fc19e-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc19e-117">PARAMETERS</span></span>

### <span data-ttu-id="fc19e-118">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="fc19e-118">-CheckMd5</span></span>
<span data-ttu-id="fc19e-119">Wenn Sie den Pfad einer Datei angeben, die nicht vorhanden ist, wird diese Datei von diesem Cmdlet erstellt, und der Inhalt wird in der neuen Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="fc19e-119">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="fc19e-120">Wenn Sie einen Pfad einer Datei angeben, die bereits vorhanden ist, und Sie den Parameter *Force* angeben, wird die Datei vom Cmdlet überschrieben.</span><span class="sxs-lookup"><span data-stu-id="fc19e-120">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="fc19e-121">Wenn Sie einen Pfad zu einer vorhandenen Datei angeben und keine *Kraft* angeben, werden Sie vom Cmdlet aufgefordert, bevor Sie fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="fc19e-121">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="fc19e-122">Wenn Sie den Pfad eines Ordners angeben, versucht dieses Cmdlet, eine Datei zu erstellen, die den Namen der Azure-Speicherdatei aufweist.</span><span class="sxs-lookup"><span data-stu-id="fc19e-122">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="fc19e-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fc19e-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="fc19e-124">Wenn Sie den Pfad einer Datei angeben, die nicht vorhanden ist, wird diese Datei von diesem Cmdlet erstellt, und der Inhalt wird in der neuen Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="fc19e-124">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="fc19e-125">Wenn Sie einen Pfad einer Datei angeben, die bereits vorhanden ist, und Sie den Parameter *Force* angeben, wird die Datei vom Cmdlet überschrieben.</span><span class="sxs-lookup"><span data-stu-id="fc19e-125">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="fc19e-126">Wenn Sie einen Pfad zu einer vorhandenen Datei angeben und keine *Kraft* angeben, werden Sie vom Cmdlet aufgefordert, bevor Sie fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="fc19e-126">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="fc19e-127">Wenn Sie den Pfad eines Ordners angeben, versucht dieses Cmdlet, eine Datei zu erstellen, die den Namen der Azure-Speicherdatei aufweist.</span><span class="sxs-lookup"><span data-stu-id="fc19e-127">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="fc19e-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="fc19e-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="fc19e-129">Wenn Sie den Pfad einer Datei angeben, die nicht vorhanden ist, wird diese Datei von diesem Cmdlet erstellt, und der Inhalt wird in der neuen Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="fc19e-129">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="fc19e-130">Wenn Sie einen Pfad einer Datei angeben, die bereits vorhanden ist, und Sie den Parameter *Force* angeben, wird die Datei vom Cmdlet überschrieben.</span><span class="sxs-lookup"><span data-stu-id="fc19e-130">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="fc19e-131">Wenn Sie einen Pfad zu einer vorhandenen Datei angeben und keine *Kraft* angeben, werden Sie vom Cmdlet aufgefordert, bevor Sie fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="fc19e-131">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="fc19e-132">Wenn Sie den Pfad eines Ordners angeben, versucht dieses Cmdlet, eine Datei zu erstellen, die den Namen der Azure-Speicherdatei aufweist.</span><span class="sxs-lookup"><span data-stu-id="fc19e-132">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="fc19e-133">-Context</span><span class="sxs-lookup"><span data-stu-id="fc19e-133">-Context</span></span>
<span data-ttu-id="fc19e-134">Wenn Sie den Pfad einer Datei angeben, die nicht vorhanden ist, wird diese Datei von diesem Cmdlet erstellt, und der Inhalt wird in der neuen Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="fc19e-134">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="fc19e-135">Wenn Sie einen Pfad einer Datei angeben, die bereits vorhanden ist, und Sie den Parameter *Force* angeben, wird die Datei vom Cmdlet überschrieben.</span><span class="sxs-lookup"><span data-stu-id="fc19e-135">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="fc19e-136">Wenn Sie einen Pfad zu einer vorhandenen Datei angeben und keine *Kraft* angeben, werden Sie vom Cmdlet aufgefordert, bevor Sie fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="fc19e-136">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="fc19e-137">Wenn Sie den Pfad eines Ordners angeben, versucht dieses Cmdlet, eine Datei zu erstellen, die den Namen der Azure-Speicherdatei aufweist.</span><span class="sxs-lookup"><span data-stu-id="fc19e-137">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="fc19e-138">-Ziel</span><span class="sxs-lookup"><span data-stu-id="fc19e-138">-Destination</span></span>
<span data-ttu-id="fc19e-139">Gibt den Zielpfad an.</span><span class="sxs-lookup"><span data-stu-id="fc19e-139">Specifies the destination path.</span></span>
<span data-ttu-id="fc19e-140">Mit diesem Cmdlet wird der Dateiinhalt an den Speicherort heruntergeladen, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="fc19e-140">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>

<span data-ttu-id="fc19e-141">Wenn Sie den Pfad einer Datei angeben, die nicht vorhanden ist, wird diese Datei von diesem Cmdlet erstellt, und der Inhalt wird in der neuen Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="fc19e-141">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="fc19e-142">Wenn Sie einen Pfad einer Datei angeben, die bereits vorhanden ist, und Sie den Parameter *Force* angeben, wird die Datei vom Cmdlet überschrieben.</span><span class="sxs-lookup"><span data-stu-id="fc19e-142">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="fc19e-143">Wenn Sie einen Pfad zu einer vorhandenen Datei angeben und keine *Kraft* angeben, werden Sie vom Cmdlet aufgefordert, bevor Sie fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="fc19e-143">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="fc19e-144">Wenn Sie den Pfad eines Ordners angeben, versucht dieses Cmdlet, eine Datei zu erstellen, die den Namen der Azure-Speicherdatei aufweist.</span><span class="sxs-lookup"><span data-stu-id="fc19e-144">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="fc19e-145">-Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="fc19e-145">-Directory</span></span>
<span data-ttu-id="fc19e-146">Gibt einen Ordner als **CloudFileDirectory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="fc19e-146">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="fc19e-147">Dieses Cmdlet ruft Inhalt für eine Datei in dem Ordner ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="fc19e-147">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="fc19e-148">Verwenden Sie das New-AzureStorageDirectory-Cmdlet, um ein Verzeichnis zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="fc19e-148">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="fc19e-149">Sie können auch das Get-AzureStorageFile-Cmdlet verwenden, um ein Verzeichnis abzurufen.</span><span class="sxs-lookup"><span data-stu-id="fc19e-149">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="fc19e-150">-Datei</span><span class="sxs-lookup"><span data-stu-id="fc19e-150">-File</span></span>
<span data-ttu-id="fc19e-151">Gibt eine Datei als **clouddatei** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="fc19e-151">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="fc19e-152">Dieses Cmdlet ruft die Datei ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="fc19e-152">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="fc19e-153">Verwenden Sie das Get-AzureStorageFile-Cmdlet, um ein **clouddatei** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="fc19e-153">To obtain a **CloudFile** object, use the Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: CloudFile
Parameter Sets: File
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc19e-154">-Force</span><span class="sxs-lookup"><span data-stu-id="fc19e-154">-Force</span></span>
<span data-ttu-id="fc19e-155">Wenn Sie den Pfad einer Datei angeben, die nicht vorhanden ist, wird diese Datei von diesem Cmdlet erstellt, und der Inhalt wird in der neuen Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="fc19e-155">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="fc19e-156">Wenn Sie einen Pfad einer Datei angeben, die bereits vorhanden ist, und Sie den Parameter *Force* angeben, wird die Datei vom Cmdlet überschrieben.</span><span class="sxs-lookup"><span data-stu-id="fc19e-156">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="fc19e-157">Wenn Sie einen Pfad zu einer vorhandenen Datei angeben und keine *Kraft* angeben, werden Sie vom Cmdlet aufgefordert, bevor Sie fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="fc19e-157">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="fc19e-158">Wenn Sie den Pfad eines Ordners angeben, versucht dieses Cmdlet, eine Datei zu erstellen, die den Namen der Azure-Speicherdatei aufweist.</span><span class="sxs-lookup"><span data-stu-id="fc19e-158">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="fc19e-159">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc19e-159">-PassThru</span></span>
<span data-ttu-id="fc19e-160">Wenn Sie den Pfad einer Datei angeben, die nicht vorhanden ist, wird diese Datei von diesem Cmdlet erstellt, und der Inhalt wird in der neuen Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="fc19e-160">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="fc19e-161">Wenn Sie einen Pfad einer Datei angeben, die bereits vorhanden ist, und Sie den Parameter *Force* angeben, wird die Datei vom Cmdlet überschrieben.</span><span class="sxs-lookup"><span data-stu-id="fc19e-161">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="fc19e-162">Wenn Sie einen Pfad zu einer vorhandenen Datei angeben und keine *Kraft* angeben, werden Sie vom Cmdlet aufgefordert, bevor Sie fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="fc19e-162">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="fc19e-163">Wenn Sie den Pfad eines Ordners angeben, versucht dieses Cmdlet, eine Datei zu erstellen, die den Namen der Azure-Speicherdatei aufweist.</span><span class="sxs-lookup"><span data-stu-id="fc19e-163">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="fc19e-164">-Path</span><span class="sxs-lookup"><span data-stu-id="fc19e-164">-Path</span></span>
<span data-ttu-id="fc19e-165">Gibt den Pfad einer Datei an.</span><span class="sxs-lookup"><span data-stu-id="fc19e-165">Specifies the path of a file.</span></span>
<span data-ttu-id="fc19e-166">Dieses Cmdlet ruft den Inhalt der Datei ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="fc19e-166">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="fc19e-167">Wenn die Datei nicht vorhanden ist, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="fc19e-167">If the file does not exist, this cmdlet returns an error.</span></span>

```yaml
Type: String
Parameter Sets: ShareName, Share, Directory
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc19e-168">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="fc19e-168">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="fc19e-169">Wenn Sie den Pfad einer Datei angeben, die nicht vorhanden ist, wird diese Datei von diesem Cmdlet erstellt, und der Inhalt wird in der neuen Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="fc19e-169">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="fc19e-170">Wenn Sie einen Pfad einer Datei angeben, die bereits vorhanden ist, und Sie den Parameter *Force* angeben, wird die Datei vom Cmdlet überschrieben.</span><span class="sxs-lookup"><span data-stu-id="fc19e-170">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="fc19e-171">Wenn Sie einen Pfad zu einer vorhandenen Datei angeben und keine *Kraft* angeben, werden Sie vom Cmdlet aufgefordert, bevor Sie fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="fc19e-171">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>

<span data-ttu-id="fc19e-172">Wenn Sie den Pfad eines Ordners angeben, versucht dieses Cmdlet, eine Datei zu erstellen, die den Namen der Azure-Speicherdatei aufweist.</span><span class="sxs-lookup"><span data-stu-id="fc19e-172">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="fc19e-173">-Freigeben</span><span class="sxs-lookup"><span data-stu-id="fc19e-173">-Share</span></span>
<span data-ttu-id="fc19e-174">Gibt ein **CloudFileShare** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="fc19e-174">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="fc19e-175">Mit diesem Cmdlet wird der Inhalt der Datei in der Freigabe, die dieser Parameter angibt, heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="fc19e-175">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="fc19e-176">Verwenden Sie das Get-AzureStorageShare-Cmdlet, um ein **CloudFileShare** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="fc19e-176">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="fc19e-177">Dieses Objekt enthält den Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="fc19e-177">This object contains the storage context.</span></span>
<span data-ttu-id="fc19e-178">Wenn Sie diesen Parameter angeben, geben Sie den *context* -Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="fc19e-178">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="fc19e-179">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="fc19e-179">-ShareName</span></span>
<span data-ttu-id="fc19e-180">Gibt den Namen der Dateifreigabe an.</span><span class="sxs-lookup"><span data-stu-id="fc19e-180">Specifies the name of the file share.</span></span>
<span data-ttu-id="fc19e-181">Mit diesem Cmdlet wird der Inhalt der Datei in der Freigabe, die dieser Parameter angibt, heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="fc19e-181">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="fc19e-182">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fc19e-182">-Confirm</span></span>
<span data-ttu-id="fc19e-183">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fc19e-183">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc19e-184">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc19e-184">-WhatIf</span></span>
<span data-ttu-id="fc19e-185">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fc19e-185">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc19e-186">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fc19e-186">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc19e-187">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc19e-187">CommonParameters</span></span>
<span data-ttu-id="fc19e-188">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc19e-188">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc19e-189">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc19e-189">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc19e-190">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fc19e-190">INPUTS</span></span>

### <span data-ttu-id="fc19e-191">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="fc19e-191">IStorageContext</span></span>

<span data-ttu-id="fc19e-192">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="fc19e-192">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="fc19e-193">CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="fc19e-193">CloudFileDirectory</span></span>

<span data-ttu-id="fc19e-194">Der Parameter "Verzeichnis" akzeptiert den Wert vom Typ "CloudFileDirectory" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="fc19e-194">Parameter 'Directory' accepts value of type 'CloudFileDirectory' from the pipeline</span></span>

### <span data-ttu-id="fc19e-195">Clouddatei</span><span class="sxs-lookup"><span data-stu-id="fc19e-195">CloudFile</span></span>

<span data-ttu-id="fc19e-196">Der Parameter "Datei" akzeptiert den Wert vom Typ "clouddatei" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="fc19e-196">Parameter 'File' accepts value of type 'CloudFile' from the pipeline</span></span>

### <span data-ttu-id="fc19e-197">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="fc19e-197">CloudFileShare</span></span>

<span data-ttu-id="fc19e-198">Der Parameter "Share" akzeptiert den Wert vom Typ "CloudFileShare" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="fc19e-198">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="fc19e-199">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fc19e-199">OUTPUTS</span></span>

## <span data-ttu-id="fc19e-200">Notizen</span><span class="sxs-lookup"><span data-stu-id="fc19e-200">NOTES</span></span>

## <span data-ttu-id="fc19e-201">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fc19e-201">RELATED LINKS</span></span>

[<span data-ttu-id="fc19e-202">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="fc19e-202">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="fc19e-203">Satz-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="fc19e-203">Set-AzureStorageFileContent</span></span>](./Set-AzureStorageFileContent.md)


