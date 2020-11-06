---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 18E1AD70-42A6-47A2-A685-6E218B6DC4BE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVhd.md
ms.openlocfilehash: cc43308f0e0051a050b3983968d9c86f67ec66b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505141"
---
# <span data-ttu-id="1a311-101">Save-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="1a311-101">Save-AzureRmVhd</span></span>

## <span data-ttu-id="1a311-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1a311-102">SYNOPSIS</span></span>
<span data-ttu-id="1a311-103">Speichert heruntergeladene VHD-Bilder lokal.</span><span class="sxs-lookup"><span data-stu-id="1a311-103">Saves downloaded .vhd images locally.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a311-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a311-104">SYNTAX</span></span>

### <span data-ttu-id="1a311-105">ResourceGroupParameterSetName</span><span class="sxs-lookup"><span data-stu-id="1a311-105">ResourceGroupParameterSetName</span></span>
```
Save-AzureRmVhd [-ResourceGroupName] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a311-106">StorageKeyParameterSetName</span><span class="sxs-lookup"><span data-stu-id="1a311-106">StorageKeyParameterSetName</span></span>
```
Save-AzureRmVhd [-StorageKey] <String> [-SourceUri] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfThreads] <Int32>] [-OverWrite] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a311-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1a311-107">DESCRIPTION</span></span>
<span data-ttu-id="1a311-108">Das **Save-AzureRmVhd-** Cmdlet speichert VHD-Bilder aus einem BLOB, in dem Sie in einer Datei gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="1a311-108">The **Save-AzureRmVhd** cmdlet saves .vhd images from a blob where they are stored to a file.</span></span>
<span data-ttu-id="1a311-109">Sie können die Anzahl der Downloader-Threads angeben, die der Prozess verwendet, und angeben, ob eine bereits vorhandene Datei ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1a311-109">You can specify the number of downloader threads that the process uses and whether to replace a file that already exists.</span></span>

<span data-ttu-id="1a311-110">Mit diesem Cmdlet werden Inhalte so heruntergeladen, wie Sie sind.</span><span class="sxs-lookup"><span data-stu-id="1a311-110">This cmdlet downloads content as it is.</span></span>
<span data-ttu-id="1a311-111">Es wird keine VHD-Formatkonvertierung (Virtual Hard Disk) angewendet.</span><span class="sxs-lookup"><span data-stu-id="1a311-111">It does not apply any Virtual Hard Disk (VHD) format conversion.</span></span>

## <span data-ttu-id="1a311-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1a311-112">EXAMPLES</span></span>

### <span data-ttu-id="1a311-113">Beispiel 1: Herunterladen eines Bilds</span><span class="sxs-lookup"><span data-stu-id="1a311-113">Example 1: Download an image</span></span>
```
PS C:\> Save-AzureRmVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="1a311-114">Dieser Befehl downloadet eine VHD-Datei und speichert Sie im lokalen Pfad C:\vhd\Win7Image.vhd.</span><span class="sxs-lookup"><span data-stu-id="1a311-114">This command downloads a .vhd file, and stores it in the local path C:\vhd\Win7Image.vhd.</span></span>

### <span data-ttu-id="1a311-115">Beispiel 2: Herunterladen eines Bilds und Überschreiben der lokalen Datei</span><span class="sxs-lookup"><span data-stu-id="1a311-115">Example 2: Download an image and overwrite the local file</span></span>
```
PS C:\> Save-AzureRmVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="1a311-116">Dieser Befehl downloadet eine VHD-Datei und speichert Sie im lokalen Pfad.</span><span class="sxs-lookup"><span data-stu-id="1a311-116">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="1a311-117">Der Befehl enthält den Parameter *overwrite* .</span><span class="sxs-lookup"><span data-stu-id="1a311-117">The command includes the *Overwrite* parameter.</span></span>
<span data-ttu-id="1a311-118">Wenn C:\vhd\Win7Image.VHD bereits vorhanden ist, wird es durch diesen Befehl ersetzt.</span><span class="sxs-lookup"><span data-stu-id="1a311-118">Therefore, if C:\vhd\Win7Image.vhd already exists, this command replaces it.</span></span>

### <span data-ttu-id="1a311-119">Beispiel 3: Herunterladen eines Bilds mithilfe einer angegebenen Anzahl von Threads</span><span class="sxs-lookup"><span data-stu-id="1a311-119">Example 3: Download an image by using a specified number of threads</span></span>
```
PS C:\> Save-AzureRmVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32
```

<span data-ttu-id="1a311-120">Dieser Befehl downloadet eine VHD-Datei und speichert Sie im lokalen Pfad.</span><span class="sxs-lookup"><span data-stu-id="1a311-120">This command downloads a .vhd file, and stores it in the local path.</span></span>
<span data-ttu-id="1a311-121">Der Befehl gibt einen Wert von 32 für den *NumberOfThreads* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="1a311-121">The command specifies a value of 32 for the *NumberOfThreads* parameter.</span></span>
<span data-ttu-id="1a311-122">Daher verwendet das Cmdlet 32-Threads für diese Aktion.</span><span class="sxs-lookup"><span data-stu-id="1a311-122">Therefore, the cmdlet uses 32 threads for this action.</span></span>

### <span data-ttu-id="1a311-123">Beispiel 4: Herunterladen eines Bilds und angeben des Speicher Schlüssels</span><span class="sxs-lookup"><span data-stu-id="1a311-123">Example 4: Download an image and specify the storage key</span></span>
```
PS C:\> Save-AzureRmVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw=="
```

<span data-ttu-id="1a311-124">Mit diesem Befehl wird eine VHD-Datei heruntergeladen und der Speicherschlüssel angegeben.</span><span class="sxs-lookup"><span data-stu-id="1a311-124">This command downloads a .vhd file and specifies the storage key.</span></span>

## <span data-ttu-id="1a311-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a311-125">PARAMETERS</span></span>

### <span data-ttu-id="1a311-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a311-126">-DefaultProfile</span></span>
<span data-ttu-id="1a311-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1a311-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a311-128">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="1a311-128">-LocalFilePath</span></span>
<span data-ttu-id="1a311-129">Gibt den lokalen Dateipfad des gespeicherten Bilds an.</span><span class="sxs-lookup"><span data-stu-id="1a311-129">Specifies the local file path of the saved image.</span></span>

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a311-130">-NumberOfThreads</span><span class="sxs-lookup"><span data-stu-id="1a311-130">-NumberOfThreads</span></span>
<span data-ttu-id="1a311-131">Gibt die Anzahl der Download-Threads an, die dieses Cmdlet während des Downloads verwendet.</span><span class="sxs-lookup"><span data-stu-id="1a311-131">Specifies the number of download threads that this cmdlet uses during download.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a311-132">-OverWrite</span><span class="sxs-lookup"><span data-stu-id="1a311-132">-OverWrite</span></span>
<span data-ttu-id="1a311-133">Gibt an, dass dieses Cmdlet die durch *LocalFilePath* -Datei angegebene Datei ersetzt, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1a311-133">Indicates that this cmdlet replaces the file specified by *LocalFilePath* file if it exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a311-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a311-134">-ResourceGroupName</span></span>
<span data-ttu-id="1a311-135">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="1a311-135">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a311-136">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="1a311-136">-SourceUri</span></span>
<span data-ttu-id="1a311-137">Gibt den Uniform Resource Identifier (URI) des BLOB in an `Azure` .</span><span class="sxs-lookup"><span data-stu-id="1a311-137">Specifies the Uniform Resource Identifier (URI) of the blob in `Azure`.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: src, Source

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a311-138">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="1a311-138">-StorageKey</span></span>
<span data-ttu-id="1a311-139">Gibt den Speicherschlüssel des BLOB-speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="1a311-139">Specifies the storage key of the blob storage account.</span></span>
<span data-ttu-id="1a311-140">Wenn Sie keinen Schlüssel angeben, versucht dieses Cmdlet, den Speicherschlüssel des Kontos in *SourceUri* aus Azure zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="1a311-140">If you do not specify a key, this cmdlet attempts to determine the storage key of the account in *SourceUri* from Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: StorageKeyParameterSetName
Aliases: sk

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a311-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a311-141">CommonParameters</span></span>
<span data-ttu-id="1a311-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a311-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a311-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a311-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a311-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1a311-144">INPUTS</span></span>

## <span data-ttu-id="1a311-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1a311-145">OUTPUTS</span></span>

## <span data-ttu-id="1a311-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="1a311-146">NOTES</span></span>

## <span data-ttu-id="1a311-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1a311-147">RELATED LINKS</span></span>

[<span data-ttu-id="1a311-148">Add-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="1a311-148">Add-AzureRmVhd</span></span>](./Add-AzureRMVhd.md)


