---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImageConfig.md
ms.openlocfilehash: 7c0f89d9c33dca961b822de62c05158a53195767
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503842"
---
# <span data-ttu-id="41a20-101">New-AzureRmImageConfig</span><span class="sxs-lookup"><span data-stu-id="41a20-101">New-AzureRmImageConfig</span></span>

## <span data-ttu-id="41a20-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="41a20-102">SYNOPSIS</span></span>
<span data-ttu-id="41a20-103">Erstellt ein konfigurierbares Image-Objekt.</span><span class="sxs-lookup"><span data-stu-id="41a20-103">Creates a configurable image object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41a20-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="41a20-104">SYNTAX</span></span>

```
New-AzureRmImageConfig [[-Location] <String>] [[-Tag] <Hashtable>] [[-SourceVirtualMachineId] <String>]
 [[-OsDisk] <ImageOSDisk>] [-DataDisk <ImageDataDisk[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41a20-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="41a20-105">DESCRIPTION</span></span>
<span data-ttu-id="41a20-106">Mit dem Cmdlet **New-AzureRmImageConfig** wird ein konfigurierbares Image-Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="41a20-106">The **New-AzureRmImageConfig** cmdlet creates a configurable image object.</span></span>

## <span data-ttu-id="41a20-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="41a20-107">EXAMPLES</span></span>

### <span data-ttu-id="41a20-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="41a20-108">Example 1</span></span>
```
PS C:\> $imageConfig = New-AzureRmImageConfig -Location 'West US';
PS C:\> $osDiskVhdUri = "https://contoso.blob.core.windows.net/test/os.vhd"
PS C:\> $dataDiskVhdUri1 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $dataDiskVhdUri2 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> Set-AzureRmImageOsDisk -Image $imageConfig -OsType 'Windows' -OsState 'Generalized' -BlobUri $osDiskVhdUri;
PS C:\> Add-AzureRmImageDataDisk -Image $imageConfig -Lun 1 -BlobUri $dataDiskVhdUri1;
PS C:\> Add-AzureRmImageDataDisk -Image $imageConfig -Lun 2 -BlobUri $dataDiskVhdUri2;
PS C:\> New-AzureRmImage -Image $imageConfig -ImageName 'ImageName01' -ResourceGroupName 'ResourceGroup01';
```

<span data-ttu-id="41a20-109">Der erste Befehl erstellt ein Image-Objekt und speichert es dann in der $imageConfig-Variablen.</span><span class="sxs-lookup"><span data-stu-id="41a20-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="41a20-110">Die nächsten drei Befehle weisen dem $osDiskVhdUri, $dataDiskVhdUri 1 und $dataDiskVhdUri 2-Variablen Pfade von Betriebssystemdatenträgern und zwei Datenträgern zu.</span><span class="sxs-lookup"><span data-stu-id="41a20-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="41a20-111">Dieser Ansatz dient nur zur Lesbarkeit der folgenden Befehle.</span><span class="sxs-lookup"><span data-stu-id="41a20-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="41a20-112">Mit den nächsten drei Befehlen werden dem in $imageConfig gespeicherten Bild eine Betriebssystem Diskette und zwei Datenlaufwerke hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="41a20-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="41a20-113">Der URI jedes Datenträgers wird in $osDiskVhdUri, $dataDiskVhdUri 1 und $dataDiskVhdUri 2 gespeichert.</span><span class="sxs-lookup"><span data-stu-id="41a20-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="41a20-114">Der endgültige Befehl erstellt ein Bild mit dem Namen "ImageName01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="41a20-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="41a20-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="41a20-115">PARAMETERS</span></span>

### <span data-ttu-id="41a20-116">-Datenträger</span><span class="sxs-lookup"><span data-stu-id="41a20-116">-DataDisk</span></span>
<span data-ttu-id="41a20-117">Gibt das Datenträgerobjekt an.</span><span class="sxs-lookup"><span data-stu-id="41a20-117">Specifies the data disk object.</span></span>

```yaml
Type: ImageDataDisk[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41a20-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="41a20-118">-Location</span></span>
<span data-ttu-id="41a20-119">Gibt einen Speicherort an.</span><span class="sxs-lookup"><span data-stu-id="41a20-119">Specifies a location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41a20-120">-OsDisk</span><span class="sxs-lookup"><span data-stu-id="41a20-120">-OsDisk</span></span>
<span data-ttu-id="41a20-121">Gibt den Betriebssystemdatenträger an.</span><span class="sxs-lookup"><span data-stu-id="41a20-121">Specifies the operating system Disk.</span></span>

```yaml
Type: ImageOSDisk
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41a20-122">-SourceVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="41a20-122">-SourceVirtualMachineId</span></span>
<span data-ttu-id="41a20-123">Gibt die ID der virtuellen Quellmaschine an.</span><span class="sxs-lookup"><span data-stu-id="41a20-123">Specifies the source virtual machine ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41a20-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="41a20-124">-Tag</span></span>
<span data-ttu-id="41a20-125">Gibt an, dass Ressourcen und Ressourcengruppen mit einer Reihe von Name-Wert-Paaren gekennzeichnet werden können.</span><span class="sxs-lookup"><span data-stu-id="41a20-125">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41a20-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="41a20-126">-Confirm</span></span>
<span data-ttu-id="41a20-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="41a20-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41a20-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41a20-128">-WhatIf</span></span>
<span data-ttu-id="41a20-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="41a20-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="41a20-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="41a20-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41a20-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41a20-131">CommonParameters</span></span>
<span data-ttu-id="41a20-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41a20-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41a20-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41a20-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41a20-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="41a20-134">INPUTS</span></span>

### <span data-ttu-id="41a20-135">System. String</span><span class="sxs-lookup"><span data-stu-id="41a20-135">System.String</span></span>
<span data-ttu-id="41a20-136">System. Collections. Hashtable Microsoft. Azure. Management. Compute. Models. ImageOSDisk Microsoft. Azure. Management. Compute. Models. ImageDataDisk []</span><span class="sxs-lookup"><span data-stu-id="41a20-136">System.Collections.Hashtable Microsoft.Azure.Management.Compute.Models.ImageOSDisk Microsoft.Azure.Management.Compute.Models.ImageDataDisk[]</span></span>

## <span data-ttu-id="41a20-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="41a20-137">OUTPUTS</span></span>

### <span data-ttu-id="41a20-138">Microsoft. Azure. Management. Compute. Models. Image</span><span class="sxs-lookup"><span data-stu-id="41a20-138">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="41a20-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="41a20-139">NOTES</span></span>

## <span data-ttu-id="41a20-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="41a20-140">RELATED LINKS</span></span>

