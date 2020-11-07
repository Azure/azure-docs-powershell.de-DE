---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
ms.openlocfilehash: aa1c7cebbcb6fe24b06638644d19b07c83c2ff04
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843080"
---
# <span data-ttu-id="d1d4f-101">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d1d4f-101">Get-AzStorageFileContent</span></span>

## <span data-ttu-id="d1d4f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d1d4f-102">SYNOPSIS</span></span>
<span data-ttu-id="d1d4f-103">Lädt den Inhalt einer Datei herunter.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-103">Downloads the contents of a file.</span></span>

## <span data-ttu-id="d1d4f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1d4f-104">SYNTAX</span></span>

### <span data-ttu-id="d1d4f-105">Freigabename (Standard)</span><span class="sxs-lookup"><span data-stu-id="d1d4f-105">ShareName (Default)</span></span>
```
Get-AzStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1d4f-106">Freigeben</span><span class="sxs-lookup"><span data-stu-id="d1d4f-106">Share</span></span>
```
Get-AzStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d1d4f-107">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="d1d4f-107">Directory</span></span>
```
Get-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d1d4f-108">Datei</span><span class="sxs-lookup"><span data-stu-id="d1d4f-108">File</span></span>
```
Get-AzStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d1d4f-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d1d4f-109">DESCRIPTION</span></span>
<span data-ttu-id="d1d4f-110">Das Cmdlet " **Get-AzStorageFileContent** " downloadet den Inhalt einer Datei und speichert Sie dann in einem von Ihnen angegebenen Ziel.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-110">The **Get-AzStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="d1d4f-111">Dieses Cmdlet gibt nicht den Inhalt der Datei zurück.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="d1d4f-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d1d4f-112">EXAMPLES</span></span>

### <span data-ttu-id="d1d4f-113">Beispiel 1: Herunterladen einer Datei aus einem Ordner</span><span class="sxs-lookup"><span data-stu-id="d1d4f-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="d1d4f-114">Dieser Befehl downloadet eine Datei mit dem Namen CurrentDataFile im Ordner ContosoWorkingFolder aus der Dateifreigabe ContosoShare06 in den aktuellen Ordner.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="d1d4f-115">Beispiel 2: Herunterladen der Dateien unter Beispieldatei Freigabe</span><span class="sxs-lookup"><span data-stu-id="d1d4f-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzStorageFileContent
```

<span data-ttu-id="d1d4f-116">In diesem Beispiel werden die Dateien unter Beispieldatei Freigabe heruntergeladen</span><span class="sxs-lookup"><span data-stu-id="d1d4f-116">This example downloads the files under sample file share</span></span>

## <span data-ttu-id="d1d4f-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1d4f-117">PARAMETERS</span></span>

### <span data-ttu-id="d1d4f-118">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="d1d4f-118">-CheckMd5</span></span>
<span data-ttu-id="d1d4f-119">Wenn Sie den Pfad einer Datei angeben, die nicht vorhanden ist, wird diese Datei von diesem Cmdlet erstellt, und der Inhalt wird in der neuen Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-119">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="d1d4f-120">Wenn Sie einen Pfad einer Datei angeben, die bereits vorhanden ist, und Sie den Parameter *Force* angeben, wird die Datei vom Cmdlet überschrieben.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-120">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="d1d4f-121">Wenn Sie einen Pfad zu einer vorhandenen Datei angeben und keine *Kraft* angeben, werden Sie vom Cmdlet aufgefordert, bevor Sie fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-121">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="d1d4f-122">Wenn Sie den Pfad eines Ordners angeben, versucht dieses Cmdlet, eine Datei zu erstellen, die den Namen der Azure-Speicherdatei aufweist.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-122">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="d1d4f-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d1d4f-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d1d4f-124">Wenn Sie den Pfad einer Datei angeben, die nicht vorhanden ist, wird diese Datei von diesem Cmdlet erstellt, und der Inhalt wird in der neuen Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-124">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="d1d4f-125">Wenn Sie einen Pfad einer Datei angeben, die bereits vorhanden ist, und Sie den Parameter *Force* angeben, wird die Datei vom Cmdlet überschrieben.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-125">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="d1d4f-126">Wenn Sie einen Pfad zu einer vorhandenen Datei angeben und keine *Kraft* angeben, werden Sie vom Cmdlet aufgefordert, bevor Sie fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-126">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="d1d4f-127">Wenn Sie den Pfad eines Ordners angeben, versucht dieses Cmdlet, eine Datei zu erstellen, die den Namen der Azure-Speicherdatei aufweist.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-127">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="d1d4f-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d1d4f-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d1d4f-129">Wenn Sie den Pfad einer Datei angeben, die nicht vorhanden ist, wird diese Datei von diesem Cmdlet erstellt, und der Inhalt wird in der neuen Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-129">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="d1d4f-130">Wenn Sie einen Pfad einer Datei angeben, die bereits vorhanden ist, und Sie den Parameter *Force* angeben, wird die Datei vom Cmdlet überschrieben.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-130">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="d1d4f-131">Wenn Sie einen Pfad zu einer vorhandenen Datei angeben und keine *Kraft* angeben, werden Sie vom Cmdlet aufgefordert, bevor Sie fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-131">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="d1d4f-132">Wenn Sie den Pfad eines Ordners angeben, versucht dieses Cmdlet, eine Datei zu erstellen, die den Namen der Azure-Speicherdatei aufweist.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-132">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="d1d4f-133">-Context</span><span class="sxs-lookup"><span data-stu-id="d1d4f-133">-Context</span></span>
<span data-ttu-id="d1d4f-134">Wenn Sie den Pfad einer Datei angeben, die nicht vorhanden ist, wird diese Datei von diesem Cmdlet erstellt, und der Inhalt wird in der neuen Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-134">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="d1d4f-135">Wenn Sie einen Pfad einer Datei angeben, die bereits vorhanden ist, und Sie den Parameter *Force* angeben, wird die Datei vom Cmdlet überschrieben.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-135">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="d1d4f-136">Wenn Sie einen Pfad zu einer vorhandenen Datei angeben und keine *Kraft* angeben, werden Sie vom Cmdlet aufgefordert, bevor Sie fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-136">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="d1d4f-137">Wenn Sie den Pfad eines Ordners angeben, versucht dieses Cmdlet, eine Datei zu erstellen, die den Namen der Azure-Speicherdatei aufweist.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-137">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="d1d4f-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1d4f-138">-DefaultProfile</span></span>
<span data-ttu-id="d1d4f-139">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1d4f-140">-Ziel</span><span class="sxs-lookup"><span data-stu-id="d1d4f-140">-Destination</span></span>
<span data-ttu-id="d1d4f-141">Gibt den Zielpfad an.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-141">Specifies the destination path.</span></span>
<span data-ttu-id="d1d4f-142">Mit diesem Cmdlet wird der Dateiinhalt an den Speicherort heruntergeladen, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-142">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>
<span data-ttu-id="d1d4f-143">Wenn Sie den Pfad einer Datei angeben, die nicht vorhanden ist, wird diese Datei von diesem Cmdlet erstellt, und der Inhalt wird in der neuen Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-143">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="d1d4f-144">Wenn Sie einen Pfad einer Datei angeben, die bereits vorhanden ist, und Sie den Parameter *Force* angeben, wird die Datei vom Cmdlet überschrieben.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-144">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="d1d4f-145">Wenn Sie einen Pfad zu einer vorhandenen Datei angeben und keine *Kraft* angeben, werden Sie vom Cmdlet aufgefordert, bevor Sie fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-145">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="d1d4f-146">Wenn Sie den Pfad eines Ordners angeben, versucht dieses Cmdlet, eine Datei zu erstellen, die den Namen der Azure-Speicherdatei aufweist.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-146">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="d1d4f-147">-Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="d1d4f-147">-Directory</span></span>
<span data-ttu-id="d1d4f-148">Gibt einen Ordner als **CloudFileDirectory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-148">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="d1d4f-149">Dieses Cmdlet ruft Inhalt für eine Datei in dem Ordner ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-149">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="d1d4f-150">Verwenden Sie das New-AzStorageDirectory-Cmdlet, um ein Verzeichnis zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-150">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="d1d4f-151">Sie können auch das Get-AzStorageFile-Cmdlet verwenden, um ein Verzeichnis abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-151">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1d4f-152">-Datei</span><span class="sxs-lookup"><span data-stu-id="d1d4f-152">-File</span></span>
<span data-ttu-id="d1d4f-153">Gibt eine Datei als **clouddatei** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-153">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="d1d4f-154">Dieses Cmdlet ruft die Datei ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-154">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="d1d4f-155">Verwenden Sie das Get-AzStorageFile-Cmdlet, um ein **clouddatei** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-155">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="d1d4f-156">-Force</span><span class="sxs-lookup"><span data-stu-id="d1d4f-156">-Force</span></span>
<span data-ttu-id="d1d4f-157">Wenn Sie den Pfad einer Datei angeben, die nicht vorhanden ist, wird diese Datei von diesem Cmdlet erstellt, und der Inhalt wird in der neuen Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-157">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="d1d4f-158">Wenn Sie einen Pfad einer Datei angeben, die bereits vorhanden ist, und Sie den Parameter *Force* angeben, wird die Datei vom Cmdlet überschrieben.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-158">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="d1d4f-159">Wenn Sie einen Pfad zu einer vorhandenen Datei angeben und keine *Kraft* angeben, werden Sie vom Cmdlet aufgefordert, bevor Sie fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-159">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="d1d4f-160">Wenn Sie den Pfad eines Ordners angeben, versucht dieses Cmdlet, eine Datei zu erstellen, die den Namen der Azure-Speicherdatei aufweist.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-160">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="d1d4f-161">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1d4f-161">-PassThru</span></span>
<span data-ttu-id="d1d4f-162">Wenn Sie den Pfad einer Datei angeben, die nicht vorhanden ist, wird diese Datei von diesem Cmdlet erstellt, und der Inhalt wird in der neuen Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-162">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="d1d4f-163">Wenn Sie einen Pfad einer Datei angeben, die bereits vorhanden ist, und Sie den Parameter *Force* angeben, wird die Datei vom Cmdlet überschrieben.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-163">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="d1d4f-164">Wenn Sie einen Pfad zu einer vorhandenen Datei angeben und keine *Kraft* angeben, werden Sie vom Cmdlet aufgefordert, bevor Sie fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-164">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="d1d4f-165">Wenn Sie den Pfad eines Ordners angeben, versucht dieses Cmdlet, eine Datei zu erstellen, die den Namen der Azure-Speicherdatei aufweist.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-165">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="d1d4f-166">-Path</span><span class="sxs-lookup"><span data-stu-id="d1d4f-166">-Path</span></span>
<span data-ttu-id="d1d4f-167">Gibt den Pfad einer Datei an.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-167">Specifies the path of a file.</span></span>
<span data-ttu-id="d1d4f-168">Dieses Cmdlet ruft den Inhalt der Datei ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-168">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="d1d4f-169">Wenn die Datei nicht vorhanden ist, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-169">If the file does not exist, this cmdlet returns an error.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1d4f-170">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d1d4f-170">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d1d4f-171">Wenn Sie den Pfad einer Datei angeben, die nicht vorhanden ist, wird diese Datei von diesem Cmdlet erstellt, und der Inhalt wird in der neuen Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-171">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="d1d4f-172">Wenn Sie einen Pfad einer Datei angeben, die bereits vorhanden ist, und Sie den Parameter *Force* angeben, wird die Datei vom Cmdlet überschrieben.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-172">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="d1d4f-173">Wenn Sie einen Pfad zu einer vorhandenen Datei angeben und keine *Kraft* angeben, werden Sie vom Cmdlet aufgefordert, bevor Sie fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-173">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="d1d4f-174">Wenn Sie den Pfad eines Ordners angeben, versucht dieses Cmdlet, eine Datei zu erstellen, die den Namen der Azure-Speicherdatei aufweist.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-174">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="d1d4f-175">-Freigeben</span><span class="sxs-lookup"><span data-stu-id="d1d4f-175">-Share</span></span>
<span data-ttu-id="d1d4f-176">Gibt ein **CloudFileShare** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-176">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="d1d4f-177">Mit diesem Cmdlet wird der Inhalt der Datei in der Freigabe, die dieser Parameter angibt, heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-177">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="d1d4f-178">Verwenden Sie das Get-AzStorageShare-Cmdlet, um ein **CloudFileShare** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-178">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="d1d4f-179">Dieses Objekt enthält den Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-179">This object contains the storage context.</span></span>
<span data-ttu-id="d1d4f-180">Wenn Sie diesen Parameter angeben, geben Sie den *context* -Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-180">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1d4f-181">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="d1d4f-181">-ShareName</span></span>
<span data-ttu-id="d1d4f-182">Gibt den Namen der Dateifreigabe an.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-182">Specifies the name of the file share.</span></span>
<span data-ttu-id="d1d4f-183">Mit diesem Cmdlet wird der Inhalt der Datei in der Freigabe, die dieser Parameter angibt, heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-183">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="d1d4f-184">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d1d4f-184">-Confirm</span></span>
<span data-ttu-id="d1d4f-185">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1d4f-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1d4f-186">-WhatIf</span></span>
<span data-ttu-id="d1d4f-187">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1d4f-188">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1d4f-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1d4f-189">CommonParameters</span></span>
<span data-ttu-id="d1d4f-190">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1d4f-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1d4f-191">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1d4f-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1d4f-192">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d1d4f-192">INPUTS</span></span>

### <span data-ttu-id="d1d4f-193">Microsoft. WindowsAz. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="d1d4f-193">Microsoft.WindowsAz.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="d1d4f-194">Parameter: freigeben (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d1d4f-194">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="d1d4f-195">Microsoft. WindowsAz. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="d1d4f-195">Microsoft.WindowsAz.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="d1d4f-196">Parameter: Verzeichnis (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d1d4f-196">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="d1d4f-197">Microsoft. WindowsAz. Storage. File. clouddatei</span><span class="sxs-lookup"><span data-stu-id="d1d4f-197">Microsoft.WindowsAz.Storage.File.CloudFile</span></span>
<span data-ttu-id="d1d4f-198">Parameter: Datei (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d1d4f-198">Parameters: File (ByValue)</span></span>

### <span data-ttu-id="d1d4f-199">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d1d4f-199">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d1d4f-200">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d1d4f-200">OUTPUTS</span></span>

### <span data-ttu-id="d1d4f-201">Microsoft. WindowsAz. Storage. File. clouddatei</span><span class="sxs-lookup"><span data-stu-id="d1d4f-201">Microsoft.WindowsAz.Storage.File.CloudFile</span></span>

## <span data-ttu-id="d1d4f-202">Notizen</span><span class="sxs-lookup"><span data-stu-id="d1d4f-202">NOTES</span></span>

## <span data-ttu-id="d1d4f-203">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d1d4f-203">RELATED LINKS</span></span>

[<span data-ttu-id="d1d4f-204">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="d1d4f-204">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="d1d4f-205">Satz-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="d1d4f-205">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


