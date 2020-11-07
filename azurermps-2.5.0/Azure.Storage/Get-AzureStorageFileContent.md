---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragefilecontent
schema: 2.0.0
ms.openlocfilehash: c390a51997e175efb834366a65e10d671f384fa8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848579"
---
# <span data-ttu-id="837fd-101">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="837fd-101">Get-AzureStorageFileContent</span></span>

## <span data-ttu-id="837fd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="837fd-102">SYNOPSIS</span></span>
<span data-ttu-id="837fd-103">Lädt den Inhalt einer Datei herunter.</span><span class="sxs-lookup"><span data-stu-id="837fd-103">Downloads the contents of a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="837fd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="837fd-104">SYNTAX</span></span>

### <span data-ttu-id="837fd-105">Freigabename (Standard)</span><span class="sxs-lookup"><span data-stu-id="837fd-105">ShareName (Default)</span></span>
```
Get-AzureStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="837fd-106">Freigeben</span><span class="sxs-lookup"><span data-stu-id="837fd-106">Share</span></span>
```
Get-AzureStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="837fd-107">Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="837fd-107">Directory</span></span>
```
Get-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="837fd-108">Datei</span><span class="sxs-lookup"><span data-stu-id="837fd-108">File</span></span>
```
Get-AzureStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="837fd-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="837fd-109">DESCRIPTION</span></span>
<span data-ttu-id="837fd-110">Das Cmdlet " **Get-AzureStorageFileContent** " downloadet den Inhalt einer Datei und speichert Sie dann in einem von Ihnen angegebenen Ziel.</span><span class="sxs-lookup"><span data-stu-id="837fd-110">The **Get-AzureStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="837fd-111">Dieses Cmdlet gibt nicht den Inhalt der Datei zurück.</span><span class="sxs-lookup"><span data-stu-id="837fd-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="837fd-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="837fd-112">EXAMPLES</span></span>

### <span data-ttu-id="837fd-113">Beispiel 1: Herunterladen einer Datei aus einem Ordner</span><span class="sxs-lookup"><span data-stu-id="837fd-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzureStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="837fd-114">Dieser Befehl downloadet eine Datei mit dem Namen CurrentDataFile im Ordner ContosoWorkingFolder aus der Dateifreigabe ContosoShare06 in den aktuellen Ordner.</span><span class="sxs-lookup"><span data-stu-id="837fd-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="837fd-115">Beispiel 2: Herunterladen der Dateien unter Beispieldatei Freigabe</span><span class="sxs-lookup"><span data-stu-id="837fd-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzureStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzureStorageFileContent
```

<span data-ttu-id="837fd-116">In diesem Beispiel werden die Dateien unter Beispieldatei Freigabe heruntergeladen</span><span class="sxs-lookup"><span data-stu-id="837fd-116">This example downloads the files under sample file share</span></span>

## <span data-ttu-id="837fd-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="837fd-117">PARAMETERS</span></span>

### <span data-ttu-id="837fd-118">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="837fd-118">-CheckMd5</span></span>
<span data-ttu-id="837fd-119">Wenn Sie den Pfad einer Datei angeben, die nicht vorhanden ist, wird diese Datei von diesem Cmdlet erstellt, und der Inhalt wird in der neuen Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="837fd-119">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="837fd-120">Wenn Sie einen Pfad einer Datei angeben, die bereits vorhanden ist, und Sie den Parameter *Force* angeben, wird die Datei vom Cmdlet überschrieben.</span><span class="sxs-lookup"><span data-stu-id="837fd-120">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="837fd-121">Wenn Sie einen Pfad zu einer vorhandenen Datei angeben und keine *Kraft* angeben, werden Sie vom Cmdlet aufgefordert, bevor Sie fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="837fd-121">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="837fd-122">Wenn Sie den Pfad eines Ordners angeben, versucht dieses Cmdlet, eine Datei zu erstellen, die den Namen der Azure-Speicherdatei aufweist.</span><span class="sxs-lookup"><span data-stu-id="837fd-122">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="837fd-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="837fd-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="837fd-124">Wenn Sie den Pfad einer Datei angeben, die nicht vorhanden ist, wird diese Datei von diesem Cmdlet erstellt, und der Inhalt wird in der neuen Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="837fd-124">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="837fd-125">Wenn Sie einen Pfad einer Datei angeben, die bereits vorhanden ist, und Sie den Parameter *Force* angeben, wird die Datei vom Cmdlet überschrieben.</span><span class="sxs-lookup"><span data-stu-id="837fd-125">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="837fd-126">Wenn Sie einen Pfad zu einer vorhandenen Datei angeben und keine *Kraft* angeben, werden Sie vom Cmdlet aufgefordert, bevor Sie fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="837fd-126">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="837fd-127">Wenn Sie den Pfad eines Ordners angeben, versucht dieses Cmdlet, eine Datei zu erstellen, die den Namen der Azure-Speicherdatei aufweist.</span><span class="sxs-lookup"><span data-stu-id="837fd-127">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="837fd-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="837fd-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="837fd-129">Wenn Sie den Pfad einer Datei angeben, die nicht vorhanden ist, wird diese Datei von diesem Cmdlet erstellt, und der Inhalt wird in der neuen Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="837fd-129">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="837fd-130">Wenn Sie einen Pfad einer Datei angeben, die bereits vorhanden ist, und Sie den Parameter *Force* angeben, wird die Datei vom Cmdlet überschrieben.</span><span class="sxs-lookup"><span data-stu-id="837fd-130">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="837fd-131">Wenn Sie einen Pfad zu einer vorhandenen Datei angeben und keine *Kraft* angeben, werden Sie vom Cmdlet aufgefordert, bevor Sie fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="837fd-131">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="837fd-132">Wenn Sie den Pfad eines Ordners angeben, versucht dieses Cmdlet, eine Datei zu erstellen, die den Namen der Azure-Speicherdatei aufweist.</span><span class="sxs-lookup"><span data-stu-id="837fd-132">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="837fd-133">-Context</span><span class="sxs-lookup"><span data-stu-id="837fd-133">-Context</span></span>
<span data-ttu-id="837fd-134">Wenn Sie den Pfad einer Datei angeben, die nicht vorhanden ist, wird diese Datei von diesem Cmdlet erstellt, und der Inhalt wird in der neuen Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="837fd-134">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="837fd-135">Wenn Sie einen Pfad einer Datei angeben, die bereits vorhanden ist, und Sie den Parameter *Force* angeben, wird die Datei vom Cmdlet überschrieben.</span><span class="sxs-lookup"><span data-stu-id="837fd-135">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="837fd-136">Wenn Sie einen Pfad zu einer vorhandenen Datei angeben und keine *Kraft* angeben, werden Sie vom Cmdlet aufgefordert, bevor Sie fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="837fd-136">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="837fd-137">Wenn Sie den Pfad eines Ordners angeben, versucht dieses Cmdlet, eine Datei zu erstellen, die den Namen der Azure-Speicherdatei aufweist.</span><span class="sxs-lookup"><span data-stu-id="837fd-137">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="837fd-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="837fd-138">-DefaultProfile</span></span>
<span data-ttu-id="837fd-139">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="837fd-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="837fd-140">-Ziel</span><span class="sxs-lookup"><span data-stu-id="837fd-140">-Destination</span></span>
<span data-ttu-id="837fd-141">Gibt den Zielpfad an.</span><span class="sxs-lookup"><span data-stu-id="837fd-141">Specifies the destination path.</span></span>
<span data-ttu-id="837fd-142">Mit diesem Cmdlet wird der Dateiinhalt an den Speicherort heruntergeladen, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="837fd-142">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>
<span data-ttu-id="837fd-143">Wenn Sie den Pfad einer Datei angeben, die nicht vorhanden ist, wird diese Datei von diesem Cmdlet erstellt, und der Inhalt wird in der neuen Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="837fd-143">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="837fd-144">Wenn Sie einen Pfad einer Datei angeben, die bereits vorhanden ist, und Sie den Parameter *Force* angeben, wird die Datei vom Cmdlet überschrieben.</span><span class="sxs-lookup"><span data-stu-id="837fd-144">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="837fd-145">Wenn Sie einen Pfad zu einer vorhandenen Datei angeben und keine *Kraft* angeben, werden Sie vom Cmdlet aufgefordert, bevor Sie fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="837fd-145">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="837fd-146">Wenn Sie den Pfad eines Ordners angeben, versucht dieses Cmdlet, eine Datei zu erstellen, die den Namen der Azure-Speicherdatei aufweist.</span><span class="sxs-lookup"><span data-stu-id="837fd-146">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="837fd-147">-Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="837fd-147">-Directory</span></span>
<span data-ttu-id="837fd-148">Gibt einen Ordner als **CloudFileDirectory** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="837fd-148">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="837fd-149">Dieses Cmdlet ruft Inhalt für eine Datei in dem Ordner ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="837fd-149">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="837fd-150">Verwenden Sie das New-AzureStorageDirectory-Cmdlet, um ein Verzeichnis zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="837fd-150">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="837fd-151">Sie können auch das Get-AzureStorageFile-Cmdlet verwenden, um ein Verzeichnis abzurufen.</span><span class="sxs-lookup"><span data-stu-id="837fd-151">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="837fd-152">-Datei</span><span class="sxs-lookup"><span data-stu-id="837fd-152">-File</span></span>
<span data-ttu-id="837fd-153">Gibt eine Datei als **clouddatei** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="837fd-153">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="837fd-154">Dieses Cmdlet ruft die Datei ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="837fd-154">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="837fd-155">Verwenden Sie das Get-AzureStorageFile-Cmdlet, um ein **clouddatei** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="837fd-155">To obtain a **CloudFile** object, use the Get-AzureStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="837fd-156">-Force</span><span class="sxs-lookup"><span data-stu-id="837fd-156">-Force</span></span>
<span data-ttu-id="837fd-157">Wenn Sie den Pfad einer Datei angeben, die nicht vorhanden ist, wird diese Datei von diesem Cmdlet erstellt, und der Inhalt wird in der neuen Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="837fd-157">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="837fd-158">Wenn Sie einen Pfad einer Datei angeben, die bereits vorhanden ist, und Sie den Parameter *Force* angeben, wird die Datei vom Cmdlet überschrieben.</span><span class="sxs-lookup"><span data-stu-id="837fd-158">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="837fd-159">Wenn Sie einen Pfad zu einer vorhandenen Datei angeben und keine *Kraft* angeben, werden Sie vom Cmdlet aufgefordert, bevor Sie fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="837fd-159">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="837fd-160">Wenn Sie den Pfad eines Ordners angeben, versucht dieses Cmdlet, eine Datei zu erstellen, die den Namen der Azure-Speicherdatei aufweist.</span><span class="sxs-lookup"><span data-stu-id="837fd-160">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="837fd-161">-PassThru</span><span class="sxs-lookup"><span data-stu-id="837fd-161">-PassThru</span></span>
<span data-ttu-id="837fd-162">Wenn Sie den Pfad einer Datei angeben, die nicht vorhanden ist, wird diese Datei von diesem Cmdlet erstellt, und der Inhalt wird in der neuen Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="837fd-162">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="837fd-163">Wenn Sie einen Pfad einer Datei angeben, die bereits vorhanden ist, und Sie den Parameter *Force* angeben, wird die Datei vom Cmdlet überschrieben.</span><span class="sxs-lookup"><span data-stu-id="837fd-163">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="837fd-164">Wenn Sie einen Pfad zu einer vorhandenen Datei angeben und keine *Kraft* angeben, werden Sie vom Cmdlet aufgefordert, bevor Sie fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="837fd-164">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="837fd-165">Wenn Sie den Pfad eines Ordners angeben, versucht dieses Cmdlet, eine Datei zu erstellen, die den Namen der Azure-Speicherdatei aufweist.</span><span class="sxs-lookup"><span data-stu-id="837fd-165">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="837fd-166">-Path</span><span class="sxs-lookup"><span data-stu-id="837fd-166">-Path</span></span>
<span data-ttu-id="837fd-167">Gibt den Pfad einer Datei an.</span><span class="sxs-lookup"><span data-stu-id="837fd-167">Specifies the path of a file.</span></span>
<span data-ttu-id="837fd-168">Dieses Cmdlet ruft den Inhalt der Datei ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="837fd-168">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="837fd-169">Wenn die Datei nicht vorhanden ist, gibt dieses Cmdlet einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="837fd-169">If the file does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="837fd-170">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="837fd-170">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="837fd-171">Wenn Sie den Pfad einer Datei angeben, die nicht vorhanden ist, wird diese Datei von diesem Cmdlet erstellt, und der Inhalt wird in der neuen Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="837fd-171">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="837fd-172">Wenn Sie einen Pfad einer Datei angeben, die bereits vorhanden ist, und Sie den Parameter *Force* angeben, wird die Datei vom Cmdlet überschrieben.</span><span class="sxs-lookup"><span data-stu-id="837fd-172">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="837fd-173">Wenn Sie einen Pfad zu einer vorhandenen Datei angeben und keine *Kraft* angeben, werden Sie vom Cmdlet aufgefordert, bevor Sie fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="837fd-173">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="837fd-174">Wenn Sie den Pfad eines Ordners angeben, versucht dieses Cmdlet, eine Datei zu erstellen, die den Namen der Azure-Speicherdatei aufweist.</span><span class="sxs-lookup"><span data-stu-id="837fd-174">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="837fd-175">-Freigeben</span><span class="sxs-lookup"><span data-stu-id="837fd-175">-Share</span></span>
<span data-ttu-id="837fd-176">Gibt ein **CloudFileShare** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="837fd-176">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="837fd-177">Mit diesem Cmdlet wird der Inhalt der Datei in der Freigabe, die dieser Parameter angibt, heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="837fd-177">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="837fd-178">Verwenden Sie das Get-AzureStorageShare-Cmdlet, um ein **CloudFileShare** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="837fd-178">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="837fd-179">Dieses Objekt enthält den Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="837fd-179">This object contains the storage context.</span></span>
<span data-ttu-id="837fd-180">Wenn Sie diesen Parameter angeben, geben Sie den *context* -Parameter nicht an.</span><span class="sxs-lookup"><span data-stu-id="837fd-180">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="837fd-181">-Freigabename</span><span class="sxs-lookup"><span data-stu-id="837fd-181">-ShareName</span></span>
<span data-ttu-id="837fd-182">Gibt den Namen der Dateifreigabe an.</span><span class="sxs-lookup"><span data-stu-id="837fd-182">Specifies the name of the file share.</span></span>
<span data-ttu-id="837fd-183">Mit diesem Cmdlet wird der Inhalt der Datei in der Freigabe, die dieser Parameter angibt, heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="837fd-183">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="837fd-184">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="837fd-184">-Confirm</span></span>
<span data-ttu-id="837fd-185">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="837fd-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="837fd-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="837fd-186">-WhatIf</span></span>
<span data-ttu-id="837fd-187">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="837fd-187">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="837fd-188">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="837fd-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="837fd-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="837fd-189">CommonParameters</span></span>
<span data-ttu-id="837fd-190">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="837fd-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="837fd-191">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="837fd-191">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="837fd-192">Eingaben</span><span class="sxs-lookup"><span data-stu-id="837fd-192">INPUTS</span></span>

### <span data-ttu-id="837fd-193">Microsoft. WindowsAzure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="837fd-193">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>
<span data-ttu-id="837fd-194">Parameter: freigeben (ByValue)</span><span class="sxs-lookup"><span data-stu-id="837fd-194">Parameters: Share (ByValue)</span></span>

### <span data-ttu-id="837fd-195">Microsoft. WindowsAzure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="837fd-195">Microsoft.WindowsAzure.Storage.File.CloudFileDirectory</span></span>
<span data-ttu-id="837fd-196">Parameter: Verzeichnis (ByValue)</span><span class="sxs-lookup"><span data-stu-id="837fd-196">Parameters: Directory (ByValue)</span></span>

### <span data-ttu-id="837fd-197">Microsoft. WindowsAzure. Storage. File. clouddatei</span><span class="sxs-lookup"><span data-stu-id="837fd-197">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>
<span data-ttu-id="837fd-198">Parameter: Datei (ByValue)</span><span class="sxs-lookup"><span data-stu-id="837fd-198">Parameters: File (ByValue)</span></span>

### <span data-ttu-id="837fd-199">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="837fd-199">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="837fd-200">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="837fd-200">OUTPUTS</span></span>

### <span data-ttu-id="837fd-201">Microsoft. WindowsAzure. Storage. File. clouddatei</span><span class="sxs-lookup"><span data-stu-id="837fd-201">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="837fd-202">Notizen</span><span class="sxs-lookup"><span data-stu-id="837fd-202">NOTES</span></span>

## <span data-ttu-id="837fd-203">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="837fd-203">RELATED LINKS</span></span>

[<span data-ttu-id="837fd-204">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="837fd-204">Get-AzureStorageFile</span></span>](./Get-AzureStorageFile.md)

[<span data-ttu-id="837fd-205">Satz-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="837fd-205">Set-AzureStorageFileContent</span></span>](./Set-AzureStorageFileContent.md)


