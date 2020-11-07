---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImage.md
ms.openlocfilehash: 5f723ea475ed909ee5445f3788386a2163af697d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662754"
---
# <span data-ttu-id="6a2f9-101">New-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="6a2f9-101">New-AzureRmImage</span></span>

## <span data-ttu-id="6a2f9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6a2f9-102">SYNOPSIS</span></span>
<span data-ttu-id="6a2f9-103">Erstellt ein Bild.</span><span class="sxs-lookup"><span data-stu-id="6a2f9-103">Creates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a2f9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a2f9-104">SYNTAX</span></span>

```
New-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <Image> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6a2f9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6a2f9-105">DESCRIPTION</span></span>
<span data-ttu-id="6a2f9-106">Das Cmdlet **New-AzureRmImage** erstellt ein Bild.</span><span class="sxs-lookup"><span data-stu-id="6a2f9-106">The **New-AzureRmImage** cmdlet creates an image.</span></span>

## <span data-ttu-id="6a2f9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6a2f9-107">EXAMPLES</span></span>

### <span data-ttu-id="6a2f9-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6a2f9-108">Example 1</span></span>
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

<span data-ttu-id="6a2f9-109">Der erste Befehl erstellt ein Image-Objekt und speichert es dann in der $imageConfig-Variablen.</span><span class="sxs-lookup"><span data-stu-id="6a2f9-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="6a2f9-110">Die nächsten drei Befehle weisen dem $osDiskVhdUri, $dataDiskVhdUri 1 und $dataDiskVhdUri 2-Variablen Pfade von Betriebssystemdatenträgern und zwei Datenträgern zu.</span><span class="sxs-lookup"><span data-stu-id="6a2f9-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="6a2f9-111">Dieser Ansatz dient nur zur Lesbarkeit der folgenden Befehle.</span><span class="sxs-lookup"><span data-stu-id="6a2f9-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="6a2f9-112">Mit den nächsten drei Befehlen werden dem in $imageConfig gespeicherten Bild eine Betriebssystem Diskette und zwei Datenlaufwerke hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6a2f9-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="6a2f9-113">Der URI jedes Datenträgers wird in $osDiskVhdUri, $dataDiskVhdUri 1 und $dataDiskVhdUri 2 gespeichert.</span><span class="sxs-lookup"><span data-stu-id="6a2f9-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="6a2f9-114">Der endgültige Befehl erstellt ein Bild mit dem Namen "ImageName01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="6a2f9-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="6a2f9-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a2f9-115">PARAMETERS</span></span>

### <span data-ttu-id="6a2f9-116">-Bild</span><span class="sxs-lookup"><span data-stu-id="6a2f9-116">-Image</span></span>
<span data-ttu-id="6a2f9-117">Gibt ein lokales Image-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="6a2f9-117">Specifies a local image object.</span></span>

```yaml
Type: Image
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a2f9-118">-Bildname</span><span class="sxs-lookup"><span data-stu-id="6a2f9-118">-ImageName</span></span>
<span data-ttu-id="6a2f9-119">Gibt den Namen eines Bilds an.</span><span class="sxs-lookup"><span data-stu-id="6a2f9-119">Specifies the name of an image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a2f9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a2f9-120">-ResourceGroupName</span></span>
<span data-ttu-id="6a2f9-121">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="6a2f9-121">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a2f9-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6a2f9-122">-Confirm</span></span>
<span data-ttu-id="6a2f9-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6a2f9-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a2f9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a2f9-124">-WhatIf</span></span>
<span data-ttu-id="6a2f9-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6a2f9-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a2f9-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6a2f9-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a2f9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a2f9-127">CommonParameters</span></span>
<span data-ttu-id="6a2f9-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a2f9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a2f9-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a2f9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a2f9-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6a2f9-130">INPUTS</span></span>

### <span data-ttu-id="6a2f9-131">System. String</span><span class="sxs-lookup"><span data-stu-id="6a2f9-131">System.String</span></span>
<span data-ttu-id="6a2f9-132">Microsoft. Azure. Management. Compute. Models. Image</span><span class="sxs-lookup"><span data-stu-id="6a2f9-132">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="6a2f9-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6a2f9-133">OUTPUTS</span></span>

### <span data-ttu-id="6a2f9-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="6a2f9-134">System.Object</span></span>

## <span data-ttu-id="6a2f9-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="6a2f9-135">NOTES</span></span>

## <span data-ttu-id="6a2f9-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6a2f9-136">RELATED LINKS</span></span>

