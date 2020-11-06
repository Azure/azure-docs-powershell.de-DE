---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmImage.md
ms.openlocfilehash: 02255fd8fd4db5747c820755bfd46ee3251aab9e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477326"
---
# <span data-ttu-id="79c3b-101">New-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="79c3b-101">New-AzureRmImage</span></span>

## <span data-ttu-id="79c3b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="79c3b-102">SYNOPSIS</span></span>
<span data-ttu-id="79c3b-103">Erstellt ein Bild.</span><span class="sxs-lookup"><span data-stu-id="79c3b-103">Creates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79c3b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="79c3b-104">SYNTAX</span></span>

```
New-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <PSImage>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79c3b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="79c3b-105">DESCRIPTION</span></span>
<span data-ttu-id="79c3b-106">Das Cmdlet **New-AzureRmImage** erstellt ein Bild.</span><span class="sxs-lookup"><span data-stu-id="79c3b-106">The **New-AzureRmImage** cmdlet creates an image.</span></span>

## <span data-ttu-id="79c3b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="79c3b-107">EXAMPLES</span></span>

### <span data-ttu-id="79c3b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="79c3b-108">Example 1</span></span>
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

<span data-ttu-id="79c3b-109">Der erste Befehl erstellt ein Image-Objekt und speichert es dann in der $imageConfig-Variablen.</span><span class="sxs-lookup"><span data-stu-id="79c3b-109">The first command creates an image object, and then stores it in the $imageConfig variable.</span></span>

<span data-ttu-id="79c3b-110">Die nächsten drei Befehle weisen dem $osDiskVhdUri, $dataDiskVhdUri 1 und $dataDiskVhdUri 2-Variablen Pfade von Betriebssystemdatenträgern und zwei Datenträgern zu.</span><span class="sxs-lookup"><span data-stu-id="79c3b-110">The next three commands assign paths of os disk and two data disks to the $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2 variables.</span></span>
<span data-ttu-id="79c3b-111">Dieser Ansatz dient nur zur Lesbarkeit der folgenden Befehle.</span><span class="sxs-lookup"><span data-stu-id="79c3b-111">This approach is only for readability of the following commands.</span></span>

<span data-ttu-id="79c3b-112">Mit den nächsten drei Befehlen werden dem in $imageConfig gespeicherten Bild eine Betriebssystem Diskette und zwei Datenlaufwerke hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="79c3b-112">The next three commands each adds an os disk and two data disks to the image stored in $imageConfig.</span></span>
<span data-ttu-id="79c3b-113">Der URI jedes Datenträgers wird in $osDiskVhdUri, $dataDiskVhdUri 1 und $dataDiskVhdUri 2 gespeichert.</span><span class="sxs-lookup"><span data-stu-id="79c3b-113">The URI of each disk is stored in $osDiskVhdUri, $dataDiskVhdUri1, and $dataDiskVhdUri2.</span></span>

<span data-ttu-id="79c3b-114">Der endgültige Befehl erstellt ein Bild mit dem Namen "ImageName01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="79c3b-114">The final command creates an image named 'ImageName01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="79c3b-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="79c3b-115">PARAMETERS</span></span>

### <span data-ttu-id="79c3b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79c3b-116">-DefaultProfile</span></span>
<span data-ttu-id="79c3b-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="79c3b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79c3b-118">-Bild</span><span class="sxs-lookup"><span data-stu-id="79c3b-118">-Image</span></span>
<span data-ttu-id="79c3b-119">Gibt ein lokales Image-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="79c3b-119">Specifies a local image object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSImage
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79c3b-120">-Bildname</span><span class="sxs-lookup"><span data-stu-id="79c3b-120">-ImageName</span></span>
<span data-ttu-id="79c3b-121">Gibt den Namen eines Bilds an.</span><span class="sxs-lookup"><span data-stu-id="79c3b-121">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79c3b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79c3b-122">-ResourceGroupName</span></span>
<span data-ttu-id="79c3b-123">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="79c3b-123">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79c3b-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="79c3b-124">-Confirm</span></span>
<span data-ttu-id="79c3b-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="79c3b-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79c3b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79c3b-126">-WhatIf</span></span>
<span data-ttu-id="79c3b-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="79c3b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79c3b-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="79c3b-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79c3b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79c3b-129">CommonParameters</span></span>
<span data-ttu-id="79c3b-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79c3b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79c3b-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79c3b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79c3b-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="79c3b-132">INPUTS</span></span>

### <span data-ttu-id="79c3b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="79c3b-133">System.String</span></span>
<span data-ttu-id="79c3b-134">Microsoft. Azure. Management. Compute. Models. Image</span><span class="sxs-lookup"><span data-stu-id="79c3b-134">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="79c3b-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="79c3b-135">OUTPUTS</span></span>

### <span data-ttu-id="79c3b-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="79c3b-136">System.Object</span></span>

## <span data-ttu-id="79c3b-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="79c3b-137">NOTES</span></span>

## <span data-ttu-id="79c3b-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="79c3b-138">RELATED LINKS</span></span>

