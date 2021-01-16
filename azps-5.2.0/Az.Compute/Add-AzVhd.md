---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D08DAA8B-B7BF-4167-AB16-F2723985A0B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVhd.md
ms.openlocfilehash: d0031ad2a6b4c38937e7faaf0743d6181608ff15
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98305832"
---
# <span data-ttu-id="c5520-101">Add-AzVhd</span><span class="sxs-lookup"><span data-stu-id="c5520-101">Add-AzVhd</span></span>

## <span data-ttu-id="c5520-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5520-102">SYNOPSIS</span></span>
<span data-ttu-id="c5520-103">Lädt eine virtuelle Festplatte von einem lokalen virtuellen Computer in ein BLOB in einem Cloudspeicherkonto in Azure hoch.</span><span class="sxs-lookup"><span data-stu-id="c5520-103">Uploads a virtual hard disk from an on-premises virtual machine to a blob in a cloud storage account in Azure.</span></span>

## <span data-ttu-id="c5520-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c5520-104">SYNTAX</span></span>

```
Add-AzVhd [[-ResourceGroupName] <String>] [-Destination] <Uri> [-LocalFilePath] <FileInfo>
 [[-NumberOfUploaderThreads] <Int32>] [[-BaseImageUriToPatch] <Uri>] [-OverWrite] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5520-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c5520-105">DESCRIPTION</span></span>
<span data-ttu-id="c5520-106">Das **Add-AzVhd-Cmdlet** lädt lokale virtuelle Festplatten im VHD-Dateiformat als feste virtuelle Festplatten in ein BLOB-Speicherkonto hoch.</span><span class="sxs-lookup"><span data-stu-id="c5520-106">The **Add-AzVhd** cmdlet uploads on-premises virtual hard disks, in .vhd file format, to a blob storage account as fixed virtual hard disks.</span></span>
<span data-ttu-id="c5520-107">Sie können die Anzahl der Uploaderthreads konfigurieren, die verwendet werden, oder ein vorhandenes BLOB im angegebenen Ziel-URI überschreiben.</span><span class="sxs-lookup"><span data-stu-id="c5520-107">You can configure the number of uploader threads that will be used or overwrite an existing blob in the specified destination URI.</span></span>
<span data-ttu-id="c5520-108">Außerdem wird die Möglichkeit unterstützt, eine patchierte Version einer lokalen VHD-Datei hochzuladen.</span><span class="sxs-lookup"><span data-stu-id="c5520-108">Also supported is the ability to upload a patched version of an on-premises .vhd file.</span></span>
<span data-ttu-id="c5520-109">Wenn bereits eine virtuelle Basisfestplatte hochgeladen wurde, können Sie andere Datenträger hochladen, die das Basisbild als übergeordnetes Bild verwenden.</span><span class="sxs-lookup"><span data-stu-id="c5520-109">When a base virtual hard disk has already been uploaded, you can upload differencing disks that use the base image as the parent.</span></span>
<span data-ttu-id="c5520-110">Der SAS-URI (Shared Access Signature) wird ebenfalls unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c5520-110">Shared access signature (SAS) URI is supported also.</span></span>

## <span data-ttu-id="c5520-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c5520-111">EXAMPLES</span></span>

### <span data-ttu-id="c5520-112">Beispiel 1: Hinzufügen einer VHD-Datei</span><span class="sxs-lookup"><span data-stu-id="c5520-112">Example 1: Add a VHD file</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd"
```

<span data-ttu-id="c5520-113">Mit diesem Befehl wird einem Speicherkonto eine VHD-Datei hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="c5520-113">This command adds a .vhd file to a storage account.</span></span>

### <span data-ttu-id="c5520-114">Beispiel 2: Hinzufügen einer VHD-Datei und Überschreiben des Ziels</span><span class="sxs-lookup"><span data-stu-id="c5520-114">Example 2: Add a VHD file and overwrite the destination</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -Overwrite
```

<span data-ttu-id="c5520-115">Mit diesem Befehl wird einem Speicherkonto eine VHD-Datei hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="c5520-115">This command adds a .vhd file to a storage account.</span></span>
<span data-ttu-id="c5520-116">Der Befehl überschreibt eine vorhandene Datei.</span><span class="sxs-lookup"><span data-stu-id="c5520-116">The command overwrites an existing file.</span></span>

### <span data-ttu-id="c5520-117">Beispiel 3: Hinzufügen einer VHD-Datei und Angeben der Anzahl von Threads</span><span class="sxs-lookup"><span data-stu-id="c5520-117">Example 3: Add a VHD file and specify the number of threads</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd" -LocalFilePath "C:\vhd\Win7Image.vhd" -NumberOfUploaderThreads 32
```

<span data-ttu-id="c5520-118">Mit diesem Befehl wird einem Speicherkonto eine VHD-Datei hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="c5520-118">This command adds a .vhd file to a storage account.</span></span>
<span data-ttu-id="c5520-119">Der Befehl gibt die Anzahl der Threads an, die zum Hochladen der Datei verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c5520-119">The command specifies the number of threads to use to upload the file.</span></span>

### <span data-ttu-id="c5520-120">Beispiel 4: Hinzufügen einer VHD-Datei und Angeben des SAS-URI</span><span class="sxs-lookup"><span data-stu-id="c5520-120">Example 4: Add a VHD file and specify the SAS URI</span></span>
```
PS C:\> Add-AzVhd -Destination "http://contosoaccount.blob.core.windows.net/vhdstore/win7baseimage.vhd?st=2013-01 -09T22%3A15%3A49Z&amp;se=2013-01-09T23%3A10%3A49Z&amp;sr=b&amp;sp=w&amp;sig=13T9Ow%2FRJAMmhfO%2FaP3HhKKJ6AY093SmveO SIV4%2FR7w%3D" -LocalFilePath "C:\vhd\win7baseimage.vhd"
```

<span data-ttu-id="c5520-121">Dieser Befehl fügt einem Speicherkonto eine vhd-Datei hinzu und gibt den SAS-URI an.</span><span class="sxs-lookup"><span data-stu-id="c5520-121">This command adds a .vhd file to a storage account and specifies the SAS URI.</span></span>

## <span data-ttu-id="c5520-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5520-122">PARAMETERS</span></span>

### <span data-ttu-id="c5520-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c5520-123">-AsJob</span></span>
<span data-ttu-id="c5520-124">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt nachverfolgt zu können.</span><span class="sxs-lookup"><span data-stu-id="c5520-124">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c5520-125">-BaseImageUriToPatch</span><span class="sxs-lookup"><span data-stu-id="c5520-125">-BaseImageUriToPatch</span></span>
<span data-ttu-id="c5520-126">Gibt den URI für ein Basisbild-BLOB im Azure Blob Storage an.</span><span class="sxs-lookup"><span data-stu-id="c5520-126">Specifies the URI to a base image blob in Azure Blob Storage.</span></span>
<span data-ttu-id="c5520-127">Eine SAS kann als Wert für diesen Parameter angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c5520-127">An SAS can be specified as the value for this parameter.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: bs

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5520-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5520-128">-DefaultProfile</span></span>
<span data-ttu-id="c5520-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c5520-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5520-130">-Destination</span><span class="sxs-lookup"><span data-stu-id="c5520-130">-Destination</span></span>
<span data-ttu-id="c5520-131">Gibt den URI eines BLOB im Blob Storage an.</span><span class="sxs-lookup"><span data-stu-id="c5520-131">Specifies the URI of a blob in Blob Storage.</span></span>
<span data-ttu-id="c5520-132">Der Parameter unterstützt SAS-URI, obwohl das Ziel für Patchszenarien kein SAS-URI sein kann.</span><span class="sxs-lookup"><span data-stu-id="c5520-132">The parameter supports SAS URI, although patching scenarios destination cannot be an SAS URI.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: dst

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5520-133">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="c5520-133">-LocalFilePath</span></span>
<span data-ttu-id="c5520-134">Gibt den Pfad der lokalen VHD-Datei an.</span><span class="sxs-lookup"><span data-stu-id="c5520-134">Specifies the path of the local .vhd file.</span></span>

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: lf

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5520-135">-NumberOfUploaderThreads</span><span class="sxs-lookup"><span data-stu-id="c5520-135">-NumberOfUploaderThreads</span></span>
<span data-ttu-id="c5520-136">Gibt die Anzahl der Uploadthreads an, die beim Hochladen der VHD-Datei verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c5520-136">Specifies the number of uploader threads to be used when uploading the .vhd file.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: th

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5520-137">-OverWrite</span><span class="sxs-lookup"><span data-stu-id="c5520-137">-OverWrite</span></span>
<span data-ttu-id="c5520-138">Gibt an, dass dieses Cmdlet ein vorhandenes BLOB im angegebenen Ziel-URI überschreibt( sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="c5520-138">Indicates that this cmdlet overwrites an existing blob in the specified destination URI, if one exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: o

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5520-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5520-139">-ResourceGroupName</span></span>
<span data-ttu-id="c5520-140">Gibt den Namen der Ressourcengruppe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="c5520-140">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5520-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5520-141">CommonParameters</span></span>
<span data-ttu-id="c5520-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5520-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5520-143">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c5520-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5520-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c5520-144">INPUTS</span></span>

### <span data-ttu-id="c5520-145">System.String</span><span class="sxs-lookup"><span data-stu-id="c5520-145">System.String</span></span>

### <span data-ttu-id="c5520-146">System.URI</span><span class="sxs-lookup"><span data-stu-id="c5520-146">System.Uri</span></span>

### <span data-ttu-id="c5520-147">System.IO.FileInfo</span><span class="sxs-lookup"><span data-stu-id="c5520-147">System.IO.FileInfo</span></span>

### <span data-ttu-id="c5520-148">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c5520-148">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c5520-149">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c5520-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c5520-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c5520-150">OUTPUTS</span></span>

### <span data-ttu-id="c5520-151">Microsoft.Azure.Commands.Compute.Models.VhdUploadContext</span><span class="sxs-lookup"><span data-stu-id="c5520-151">Microsoft.Azure.Commands.Compute.Models.VhdUploadContext</span></span>

## <span data-ttu-id="c5520-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c5520-152">NOTES</span></span>

## <span data-ttu-id="c5520-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c5520-153">RELATED LINKS</span></span>

[<span data-ttu-id="c5520-154">Save-AzVhd</span><span class="sxs-lookup"><span data-stu-id="c5520-154">Save-AzVhd</span></span>](./Save-AzVhd.md)


