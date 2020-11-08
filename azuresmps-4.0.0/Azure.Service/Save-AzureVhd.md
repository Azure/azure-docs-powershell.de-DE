---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E4660D0A-26CB-488C-9A29-3ED94A0DCDA2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e62cb7ed272a5c0d5ff4ff0ecbafe30a0c5ee9e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005667"
---
# <span data-ttu-id="d4e0c-101">Save-AzureVhd</span><span class="sxs-lookup"><span data-stu-id="d4e0c-101">Save-AzureVhd</span></span>

## <span data-ttu-id="d4e0c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d4e0c-102">SYNOPSIS</span></span>
<span data-ttu-id="d4e0c-103">Ermöglicht den Download von VHD-Bildern.</span><span class="sxs-lookup"><span data-stu-id="d4e0c-103">Enables download of .vhd images.</span></span>

## <span data-ttu-id="d4e0c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4e0c-104">SYNTAX</span></span>

```
Save-AzureVhd [-Source] <Uri> [-LocalFilePath] <FileInfo> [[-NumberOfThreads] <Int32>] [[-StorageKey] <String>]
 [-OverWrite] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d4e0c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d4e0c-105">DESCRIPTION</span></span>
<span data-ttu-id="d4e0c-106">Das Cmdlet **Save-AzureVhd** ermöglicht das Herunterladen von VHD-Bildern aus einem BLOB, in dem Sie in einer Datei gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="d4e0c-106">The **Save-AzureVhd** cmdlet enables download of .vhd images from a blob where they are stored to a file.</span></span>
<span data-ttu-id="d4e0c-107">Sie enthält Parameter zum Konfigurieren des Downloadprozesses, indem Sie die Anzahl der Downloader-Threads angibt, die verwendet werden, oder die Datei überschrieben wird, die bereits im angegebenen Dateipfad vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d4e0c-107">It has parameters to configure the download process by specifying the number of downloader threads that are used or overwriting the file which already exists in the specified file path.</span></span>

<span data-ttu-id="d4e0c-108">Mit **Save-AzureVhd** wird keine VHD-Formatkonvertierung durchführen, und das BLOB wird so heruntergeladen, wie es ist.</span><span class="sxs-lookup"><span data-stu-id="d4e0c-108">**Save-AzureVhd** does not do any VHD format conversion and the blob is downloaded as it is.</span></span>

## <span data-ttu-id="d4e0c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d4e0c-109">EXAMPLES</span></span>

### <span data-ttu-id="d4e0c-110">Beispiel 1: Herunterladen einer VHD-Datei</span><span class="sxs-lookup"><span data-stu-id="d4e0c-110">Example 1: Download a VHD file</span></span>
```
PS C:\> Save-AzureVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="d4e0c-111">Dieser Befehl downloadet eine VHD-Datei.</span><span class="sxs-lookup"><span data-stu-id="d4e0c-111">This command downloads a .vhd file.</span></span>

### <span data-ttu-id="d4e0c-112">Beispiel 2: Herunterladen einer VHD-Datei und Überschreiben der lokalen Datei</span><span class="sxs-lookup"><span data-stu-id="d4e0c-112">Example 2: Download a VHD file and overwrite the local file</span></span>
```
PS C:\> Save-AzureVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="d4e0c-113">Mit diesem Befehl wird eine VHD-Datei heruntergeladen und jede Datei im Zielpfad überschrieben.</span><span class="sxs-lookup"><span data-stu-id="d4e0c-113">This command downloads a .vhd file and overwrites any file in the destination path.</span></span>

### <span data-ttu-id="d4e0c-114">Beispiel 3: Herunterladen einer VHD-Datei und angeben der Anzahl der Threads</span><span class="sxs-lookup"><span data-stu-id="d4e0c-114">Example 3: Download a VHD file and specify the number of threads</span></span>
```
PS C:\> Save-AzureVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32
```

<span data-ttu-id="d4e0c-115">Mit diesem Befehl wird eine VHD-Datei heruntergeladen und die Anzahl der Threads angegeben.</span><span class="sxs-lookup"><span data-stu-id="d4e0c-115">This command downloads a .vhd file and specifies the number of threads.</span></span>

### <span data-ttu-id="d4e0c-116">Beispiel 4: Herunterladen einer VHD-Datei und angeben des Speicher Schlüssels</span><span class="sxs-lookup"><span data-stu-id="d4e0c-116">Example 4: Download a VHD file and specify the storage key</span></span>
```
PS C:\> Save-AzureVhd -Source "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -StorageKey "zNvcH0r5vAGmC5AbwEtpcyWCMyBd3eMDbdaa4ua6kwxq6vTZH3Y+sw=="
```

<span data-ttu-id="d4e0c-117">Mit diesem Befehl wird eine VHD-Datei heruntergeladen und der Speicherschlüssel angegeben.</span><span class="sxs-lookup"><span data-stu-id="d4e0c-117">This command downloads a .vhd file and specifies the storage key.</span></span>

## <span data-ttu-id="d4e0c-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4e0c-118">PARAMETERS</span></span>

### <span data-ttu-id="d4e0c-119">-Information</span><span class="sxs-lookup"><span data-stu-id="d4e0c-119">-InformationAction</span></span>
<span data-ttu-id="d4e0c-120">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="d4e0c-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d4e0c-121">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d4e0c-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d4e0c-122">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="d4e0c-122">Continue</span></span>
- <span data-ttu-id="d4e0c-123">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="d4e0c-123">Ignore</span></span>
- <span data-ttu-id="d4e0c-124">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="d4e0c-124">Inquire</span></span>
- <span data-ttu-id="d4e0c-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d4e0c-125">SilentlyContinue</span></span>
- <span data-ttu-id="d4e0c-126">Beenden</span><span class="sxs-lookup"><span data-stu-id="d4e0c-126">Stop</span></span>
- <span data-ttu-id="d4e0c-127">Anhalten</span><span class="sxs-lookup"><span data-stu-id="d4e0c-127">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4e0c-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d4e0c-128">-InformationVariable</span></span>
<span data-ttu-id="d4e0c-129">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="d4e0c-129">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4e0c-130">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="d4e0c-130">-LocalFilePath</span></span>
<span data-ttu-id="d4e0c-131">Gibt den lokalen Dateipfad an.</span><span class="sxs-lookup"><span data-stu-id="d4e0c-131">Specifies the local file path.</span></span>

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

### <span data-ttu-id="d4e0c-132">-NumberOfThreads</span><span class="sxs-lookup"><span data-stu-id="d4e0c-132">-NumberOfThreads</span></span>
<span data-ttu-id="d4e0c-133">Gibt die Anzahl der Download-Threads an, die dieses Cmdlet während des Downloads verwendet.</span><span class="sxs-lookup"><span data-stu-id="d4e0c-133">Specifies the number of download threads that this cmdlet uses during download.</span></span>

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

### <span data-ttu-id="d4e0c-134">-OverWrite</span><span class="sxs-lookup"><span data-stu-id="d4e0c-134">-OverWrite</span></span>
<span data-ttu-id="d4e0c-135">Gibt an, dass dieses Cmdlet die von *LocalFilePath* -Datei angegebene Datei löscht, wenn Sie vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d4e0c-135">Specifies that this cmdlet deletes the file specified by *LocalFilePath* file if it exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4e0c-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="d4e0c-136">-Profile</span></span>
<span data-ttu-id="d4e0c-137">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="d4e0c-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d4e0c-138">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="d4e0c-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4e0c-139">-Source</span><span class="sxs-lookup"><span data-stu-id="d4e0c-139">-Source</span></span>
<span data-ttu-id="d4e0c-140">Gibt den Uniform Resource Identifier (URI) an, in dem sich das BLOB befindet `Azure` .</span><span class="sxs-lookup"><span data-stu-id="d4e0c-140">Specifies the Uniform Resource Identifier (URI) to the blob in `Azure`.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: src

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4e0c-141">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="d4e0c-141">-StorageKey</span></span>
<span data-ttu-id="d4e0c-142">Gibt den Speicherschlüssel des BLOB-speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="d4e0c-142">Specifies the storage key of the blob storage account.</span></span>
<span data-ttu-id="d4e0c-143">Wenn Sie nicht bereitgestellt wird, versucht **Save-AzureVhd** , den Speicherschlüssel des Kontos in *SourceUri* aus Azure zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="d4e0c-143">If it is not provided, **Save-AzureVhd** attempts to determine the storage key of the account in *SourceUri* from Azure.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: sk

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4e0c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4e0c-144">CommonParameters</span></span>
<span data-ttu-id="d4e0c-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4e0c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4e0c-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4e0c-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4e0c-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d4e0c-147">INPUTS</span></span>

## <span data-ttu-id="d4e0c-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d4e0c-148">OUTPUTS</span></span>

## <span data-ttu-id="d4e0c-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="d4e0c-149">NOTES</span></span>

## <span data-ttu-id="d4e0c-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d4e0c-150">RELATED LINKS</span></span>

[<span data-ttu-id="d4e0c-151">Add-AzureVhd</span><span class="sxs-lookup"><span data-stu-id="d4e0c-151">Add-AzureVhd</span></span>](./Add-AzureVhd.md)


