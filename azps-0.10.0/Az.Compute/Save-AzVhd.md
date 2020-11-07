---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 18E1AD70-42A6-47A2-A685-6E218B6DC4BE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/save-azvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Save-AzVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Save-AzVhd.md
ms.openlocfilehash: f178b6aca1cf3747bc53807290585c01b91f3c2e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844316"
---
# <span data-ttu-id="d0907-101">Save-AzVhd</span><span class="sxs-lookup"><span data-stu-id="d0907-101">Save-AzVhd</span></span>

## <span data-ttu-id="d0907-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d0907-102">SYNOPSIS</span></span>
<span data-ttu-id="d0907-103">Speichert heruntergeladene VHD-Bilder lokal.</span><span class="sxs-lookup"><span data-stu-id="d0907-103">Saves downloaded .vhd images locally.</span></span>

## <span data-ttu-id="d0907-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0907-104">SYNTAX</span></span>

### <span data-ttu-id="d0907-105">ResourceGroupParameterSetName</span><span class="sxs-lookup"><span data-stu-id="d0907-105">ResourceGroupParameterSetName</span></span>
```
Save-AzVhd [-ResourceGroupName] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d0907-106">StorageKeyParameterSetName</span><span class="sxs-lookup"><span data-stu-id="d0907-106">StorageKeyParameterSetName</span></span>
```
Save-AzVhd [-StorageKey] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d0907-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d0907-107">DESCRIPTION</span></span>
<span data-ttu-id="d0907-108">Das **Save-AzVhd-** Cmdlet speichert VHD-Bilder aus einem BLOB, in dem Sie in einer Datei gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="d0907-108">The **Save-AzVhd** cmdlet saves .vhd images from a blob where they are stored to a file.</span></span>
<span data-ttu-id="d0907-109">Sie können die Anzahl der Downloader-Threads angeben, die der Prozess verwendet, und angeben, ob eine bereits vorhandene Datei ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d0907-109">You can specify the number of downloader threads that the process uses and whether to replace a file that already exists.</span></span>

<span data-ttu-id="d0907-110">Mit diesem Cmdlet werden Inhalte so heruntergeladen, wie Sie sind.</span><span class="sxs-lookup"><span data-stu-id="d0907-110">This cmdlet downloads content as it is.</span></span>
<span data-ttu-id="d0907-111">Es wird keine VHD-Formatkonvertierung (Virtual Hard Disk) angewendet.</span><span class="sxs-lookup"><span data-stu-id="d0907-111">It does not apply any Virtual Hard Disk (VHD) format conversion.</span></span>

## <span data-ttu-id="d0907-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d0907-112">EXAMPLES</span></span>

### <span data-ttu-id="d0907-113">Beispiel 1: Herunterladen eines Bilds</span><span class="sxs-lookup"><span data-stu-id="d0907-113">Example 1: Download an image</span></span>
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -ResourceGroupName "rgname"
```

<span data-ttu-id="d0907-114">Dieser Befehl downloadet eine VHD-Datei und speichert Sie im lokalen Pfad C:\vhd\Win7Image.vhd.</span><span class="sxs-lookup"><span data-stu-id="d0907-114">This command downloads a .vhd file, and stores it in the local path C:\vhd\Win7Image.vhd.</span></span>

### <span data-ttu-id="d0907-115">Beispiel 2: Herunterladen eines Bilds und Überschreiben der lokalen Datei</span><span class="sxs-lookup"><span data-stu-id="d0907-115">Example 2: Download an image and overwrite the local file</span></span>
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite -ResourceGroupName "rgname"
```

<span data-ttu-id="d0907-116">Dieser Befehl downloadet eine VHD-Datei und speichert Sie im lokalen Pfad.</span><span class="sxs-lookup"><span data-stu-id="d0907-116">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="d0907-117">Der Befehl enthält den Parameter *overwrite* .</span><span class="sxs-lookup"><span data-stu-id="d0907-117">The command includes the *Overwrite* parameter.</span></span>
<span data-ttu-id="d0907-118">Wenn C:\vhd\Win7Image.VHD bereits vorhanden ist, wird es durch diesen Befehl ersetzt.</span><span class="sxs-lookup"><span data-stu-id="d0907-118">Therefore, if C:\vhd\Win7Image.vhd already exists, this command replaces it.</span></span>

### <span data-ttu-id="d0907-119">Beispiel 3: Herunterladen eines Bilds mithilfe einer angegebenen Anzahl von Threads</span><span class="sxs-lookup"><span data-stu-id="d0907-119">Example 3: Download an image by using a specified number of threads</span></span>
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32 -ResourceGroupName "rgname"
```

<span data-ttu-id="d0907-120">Dieser Befehl downloadet eine VHD-Datei und speichert Sie im lokalen Pfad.</span><span class="sxs-lookup"><span data-stu-id="d0907-120">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="d0907-121">Der Befehl gibt einen Wert von 32 für den *NumberOfThreads* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="d0907-121">The command specifies a value of 32 for the *NumberOfThreads* parameter.</span></span>
<span data-ttu-id="d0907-122">Daher verwendet das Cmdlet 32-Threads für diese Aktion.</span><span class="sxs-lookup"><span data-stu-id="d0907-122">Therefore, the cmdlet uses 32 threads for this action.</span></span>

### <span data-ttu-id="d0907-123">Beispiel 4: Herunterladen eines Bilds und angeben des Speicher Schlüssels</span><span class="sxs-lookup"><span data-stu-id="d0907-123">Example 4: Download an image and specify the storage key</span></span>
```
PS C:\> Save-AzVhd -SourceUri "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw==" -ResourceGroupName "rgname"
```

<span data-ttu-id="d0907-124">Mit diesem Befehl wird eine VHD-Datei heruntergeladen und der Speicherschlüssel angegeben.</span><span class="sxs-lookup"><span data-stu-id="d0907-124">This command downloads a .vhd file and specifies the storage key.</span></span>

## <span data-ttu-id="d0907-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="d0907-125">PARAMETERS</span></span>

### <span data-ttu-id="d0907-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0907-126">-AsJob</span></span>
<span data-ttu-id="d0907-127">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="d0907-127">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d0907-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0907-128">-DefaultProfile</span></span>
<span data-ttu-id="d0907-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d0907-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0907-130">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="d0907-130">-LocalFilePath</span></span>
<span data-ttu-id="d0907-131">Gibt den lokalen Dateipfad des gespeicherten Bilds an.</span><span class="sxs-lookup"><span data-stu-id="d0907-131">Specifies the local file path of the saved image.</span></span>

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0907-132">-NumberOfThreads</span><span class="sxs-lookup"><span data-stu-id="d0907-132">-NumberOfThreads</span></span>
<span data-ttu-id="d0907-133">Gibt die Anzahl der Download-Threads an, die dieses Cmdlet während des Downloads verwendet.</span><span class="sxs-lookup"><span data-stu-id="d0907-133">Specifies the number of download threads that this cmdlet uses during download.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0907-134">-OverWrite</span><span class="sxs-lookup"><span data-stu-id="d0907-134">-OverWrite</span></span>
<span data-ttu-id="d0907-135">Gibt an, dass dieses Cmdlet die durch *LocalFilePath* -Datei angegebene Datei ersetzt, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d0907-135">Indicates that this cmdlet replaces the file specified by *LocalFilePath* file if it exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0907-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0907-136">-ResourceGroupName</span></span>
<span data-ttu-id="d0907-137">Gibt den Namen der Ressourcengruppe des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="d0907-137">Specifies the name of the resource group of the storage account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0907-138">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="d0907-138">-SourceUri</span></span>
<span data-ttu-id="d0907-139">Gibt den Uniform Resource Identifier (URI) des BLOB in an `Azure` .</span><span class="sxs-lookup"><span data-stu-id="d0907-139">Specifies the Uniform Resource Identifier (URI) of the blob in `Azure`.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: src, Source

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0907-140">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="d0907-140">-StorageKey</span></span>
<span data-ttu-id="d0907-141">Gibt den Speicherschlüssel des BLOB-speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="d0907-141">Specifies the storage key of the blob storage account.</span></span>
<span data-ttu-id="d0907-142">Wenn Sie keinen Schlüssel angeben, versucht dieses Cmdlet, den Speicherschlüssel des Kontos in *SourceUri* aus Azure zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="d0907-142">If you do not specify a key, this cmdlet attempts to determine the storage key of the account in *SourceUri* from Azure.</span></span>

```yaml
Type: String
Parameter Sets: StorageKeyParameterSetName
Aliases: sk

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0907-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0907-143">CommonParameters</span></span>
<span data-ttu-id="d0907-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0907-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0907-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0907-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0907-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d0907-146">INPUTS</span></span>

### <span data-ttu-id="d0907-147">Keine</span><span class="sxs-lookup"><span data-stu-id="d0907-147">None</span></span>
<span data-ttu-id="d0907-148">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="d0907-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d0907-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d0907-149">OUTPUTS</span></span>

### <span data-ttu-id="d0907-150">Microsoft. Azure. Commands. Compute. Models. VhdDownloadContext</span><span class="sxs-lookup"><span data-stu-id="d0907-150">Microsoft.Azure.Commands.Compute.Models.VhdDownloadContext</span></span>

## <span data-ttu-id="d0907-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="d0907-151">NOTES</span></span>

## <span data-ttu-id="d0907-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d0907-152">RELATED LINKS</span></span>

[<span data-ttu-id="d0907-153">Add-AzVhd</span><span class="sxs-lookup"><span data-stu-id="d0907-153">Add-AzVhd</span></span>](./Add-AzVhd.md)


