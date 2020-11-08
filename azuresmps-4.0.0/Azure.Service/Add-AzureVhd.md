---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 99DC239C-EA68-4830-9345-762CD6A3F68C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 320b95add2806f48121151a71bdf36a572fa05a1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005924"
---
# <span data-ttu-id="d8be3-101">Add-AzureVhd</span><span class="sxs-lookup"><span data-stu-id="d8be3-101">Add-AzureVhd</span></span>

## <span data-ttu-id="d8be3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d8be3-102">SYNOPSIS</span></span>
<span data-ttu-id="d8be3-103">Lädt eine VHD-Datei von einem lokalen Computer zu einem BLOB in einem Cloud-Speicherkonto in Azure hoch.</span><span class="sxs-lookup"><span data-stu-id="d8be3-103">Uploads a VHD file from an on-premise computer to a blob in a cloud storage account in Azure.</span></span>

## <span data-ttu-id="d8be3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8be3-104">SYNTAX</span></span>

```
Add-AzureVhd [-Destination] <Uri> [-LocalFilePath] <FileInfo> [[-NumberOfUploaderThreads] <Int32>]
 [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d8be3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d8be3-105">DESCRIPTION</span></span>
<span data-ttu-id="d8be3-106">Mit dem Cmdlet " **Add-AzureVhd** " werden virtuelle Festplatten (VHD)-Bilder in einem BLOB-Speicherkonto als feste VHD-Bilder hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="d8be3-106">The **Add-AzureVhd** cmdlet uploads on premise Virtual hard disk (VHD) images to a blob storage account as fixed .vhd images.</span></span>
<span data-ttu-id="d8be3-107">Er verfügt über Parameter zum Konfigurieren des Upload-Vorgangs, beispielsweise zum Angeben der Anzahl der Uploader-Threads, die verwendet werden, oder zum Überschreiben eines BLOB, das bereits im angegebenen Ziel-URI vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d8be3-107">It has parameters to configure the upload process such as specifying the number of uploader threads that will be used or overwriting a blob which already exists in the specified destination URI.</span></span>
<span data-ttu-id="d8be3-108">Für lokale VHD-Bilder wird ein Patch-Szenario ebenfalls unterstützt, damit unterschiedlich festgestellte Datenträger Bilder hochgeladen werden können, ohne dass die bereits hochgeladenen Basisbilder hochgeladen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="d8be3-108">For on premise VHD images, patching scenario is also supported so that diff disk images can be uploaded without having to upload the already uploaded base images.</span></span> <span data-ttu-id="d8be3-109">SAS-URI (Shared Access Signature) wird ebenfalls unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d8be3-109">Shared Access Signature (SAS) URI is also supported.</span></span>

## <span data-ttu-id="d8be3-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d8be3-110">EXAMPLES</span></span>

### <span data-ttu-id="d8be3-111">Beispiel 1: Hinzufügen einer VHD-Datei</span><span class="sxs-lookup"><span data-stu-id="d8be3-111">Example 1: Add a VHD file</span></span>
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="d8be3-112">Mit diesem Befehl wird eine VHD-Datei zu einem Speicherkonto hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d8be3-112">This command adds a .vhd file to a storage account.</span></span>

### <span data-ttu-id="d8be3-113">Beispiel 2: Hinzufügen einer VHD-Datei und Überschreiben des Ziels</span><span class="sxs-lookup"><span data-stu-id="d8be3-113">Example 2: Add a VHD file and overwrite the destination</span></span>
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="d8be3-114">Mit diesem Befehl wird eine VHD-Datei zu einem Speicherkonto hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d8be3-114">This command adds a .vhd file to a storage account.</span></span>

### <span data-ttu-id="d8be3-115">Beispiel 3: Hinzufügen einer VHD-Datei und angeben der Anzahl der Threads</span><span class="sxs-lookup"><span data-stu-id="d8be3-115">Example 3: Add a VHD file and specify the number of threads</span></span>
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfThreads 32
```

<span data-ttu-id="d8be3-116">Mit diesem Befehl wird eine VHD-Datei zu einem Speicherkonto hinzugefügt, und es wird die Anzahl der Threads angegeben, die zum Hochladen der Datei verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d8be3-116">This command adds a .vhd file to a storage account and specifies the number of threads to use to upload the file.</span></span>

### <span data-ttu-id="d8be3-117">Beispiel 4: Hinzufügen einer VHD-Datei und angeben des SAS-URIs</span><span class="sxs-lookup"><span data-stu-id="d8be3-117">Example 4: Add a VHD file and specify the SAS URI</span></span>
```
PS C:\> Add-AzureVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01-09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveOSIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

<span data-ttu-id="d8be3-118">Mit diesem Befehl wird eine VHD-Datei zu einem Speicherkonto hinzugefügt und der SAS-URI angegeben.</span><span class="sxs-lookup"><span data-stu-id="d8be3-118">This command adds a .vhd file to a storage account and specifies the SAS URI.</span></span>

## <span data-ttu-id="d8be3-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8be3-119">PARAMETERS</span></span>

### <span data-ttu-id="d8be3-120">-BaseImageUriToPatch</span><span class="sxs-lookup"><span data-stu-id="d8be3-120">-BaseImageUriToPatch</span></span>
<span data-ttu-id="d8be3-121">Gibt einen URI für ein Basis Bild-BLOB im Azure BLOB-Speicher an.</span><span class="sxs-lookup"><span data-stu-id="d8be3-121">Specifies an URI to a base image blob in Azure Blob Storage.</span></span>
<span data-ttu-id="d8be3-122">SAS in URI-Eingabe wird ebenfalls unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d8be3-122">SAS in URI input is supported as well.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: bs

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8be3-123">-Ziel</span><span class="sxs-lookup"><span data-stu-id="d8be3-123">-Destination</span></span>
<span data-ttu-id="d8be3-124">Gibt einen URI für ein BLOB im Microsoft Azure BLOB-Speicher an.</span><span class="sxs-lookup"><span data-stu-id="d8be3-124">Specifies a URI to a blob in Microsoft Azure Blob Storage.</span></span>
<span data-ttu-id="d8be3-125">SAS in URI-Eingabe wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d8be3-125">SAS in URI input is supported.</span></span>
<span data-ttu-id="d8be3-126">In Patch-Szenarien kann das Ziel jedoch kein SAS-URI sein.</span><span class="sxs-lookup"><span data-stu-id="d8be3-126">However, in patching scenarios the destination cannot be a SAS URI.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: dst

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8be3-127">-Information</span><span class="sxs-lookup"><span data-stu-id="d8be3-127">-InformationAction</span></span>
<span data-ttu-id="d8be3-128">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="d8be3-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d8be3-129">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d8be3-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d8be3-130">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="d8be3-130">Continue</span></span>
- <span data-ttu-id="d8be3-131">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="d8be3-131">Ignore</span></span>
- <span data-ttu-id="d8be3-132">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="d8be3-132">Inquire</span></span>
- <span data-ttu-id="d8be3-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d8be3-133">SilentlyContinue</span></span>
- <span data-ttu-id="d8be3-134">Beenden</span><span class="sxs-lookup"><span data-stu-id="d8be3-134">Stop</span></span>
- <span data-ttu-id="d8be3-135">Anhalten</span><span class="sxs-lookup"><span data-stu-id="d8be3-135">Suspend</span></span>

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

### <span data-ttu-id="d8be3-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d8be3-136">-InformationVariable</span></span>
<span data-ttu-id="d8be3-137">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="d8be3-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d8be3-138">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="d8be3-138">-LocalFilePath</span></span>
<span data-ttu-id="d8be3-139">Art der Dateipfad der lokalen VHD-Datei.</span><span class="sxs-lookup"><span data-stu-id="d8be3-139">Species the file path of the local .vhd file.</span></span>

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8be3-140">-NumberOfUploaderThreads</span><span class="sxs-lookup"><span data-stu-id="d8be3-140">-NumberOfUploaderThreads</span></span>
<span data-ttu-id="d8be3-141">Gibt die Anzahl der Threads an, die für den Upload verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d8be3-141">Specifies the number of threads to use for upload.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8be3-142">-OverWrite</span><span class="sxs-lookup"><span data-stu-id="d8be3-142">-OverWrite</span></span>
<span data-ttu-id="d8be3-143">Gibt an, dass dieses Cmdlet das vorhandene BLOB im angegebenen Ziel-URI löscht, wenn es vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d8be3-143">Specifies that this cmdlet deletes the existing blob in the specified destination URI if it exists.</span></span>

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

### <span data-ttu-id="d8be3-144">-Profil</span><span class="sxs-lookup"><span data-stu-id="d8be3-144">-Profile</span></span>
<span data-ttu-id="d8be3-145">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="d8be3-145">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d8be3-146">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="d8be3-146">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d8be3-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8be3-147">CommonParameters</span></span>
<span data-ttu-id="d8be3-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8be3-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8be3-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8be3-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8be3-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d8be3-150">INPUTS</span></span>

## <span data-ttu-id="d8be3-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d8be3-151">OUTPUTS</span></span>

## <span data-ttu-id="d8be3-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="d8be3-152">NOTES</span></span>

## <span data-ttu-id="d8be3-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d8be3-153">RELATED LINKS</span></span>

[<span data-ttu-id="d8be3-154">Save-AzureVhd</span><span class="sxs-lookup"><span data-stu-id="d8be3-154">Save-AzureVhd</span></span>](./Save-AzureVhd.md)


