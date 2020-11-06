---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmImage.md
ms.openlocfilehash: b7c5155706b968973bef6a5cf1ce2285caee819d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476898"
---
# <span data-ttu-id="e5f6e-101">Update-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="e5f6e-101">Update-AzureRmImage</span></span>

## <span data-ttu-id="e5f6e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e5f6e-102">SYNOPSIS</span></span>
<span data-ttu-id="e5f6e-103">Aktualisiert ein Bild.</span><span class="sxs-lookup"><span data-stu-id="e5f6e-103">Updates an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5f6e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5f6e-104">SYNTAX</span></span>

```
Update-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Image] <Image> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e5f6e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e5f6e-105">DESCRIPTION</span></span>
<span data-ttu-id="e5f6e-106">Das Cmdlet **Update-AzureRmImage** aktualisiert ein Bild.</span><span class="sxs-lookup"><span data-stu-id="e5f6e-106">The **Update-AzureRmImage** cmdlet updates an image.</span></span>

## <span data-ttu-id="e5f6e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e5f6e-107">EXAMPLES</span></span>

### <span data-ttu-id="e5f6e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e5f6e-108">Example 1</span></span>
```
PS C:\> Get-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' | Remove-AzureRmImageDataDisk -Lun 1 | Update-AzureRmImage;
```

<span data-ttu-id="e5f6e-109">Mit diesem Befehl wird der Datenträger der logischen Einheit 1 aus dem vorhandenen Bild ' Image01 ' in der Ressourcengruppe ' ResourceGroup01 ' entfernt.</span><span class="sxs-lookup"><span data-stu-id="e5f6e-109">This command removes the data disk of logical unit number 1 from the existing image 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="e5f6e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5f6e-110">PARAMETERS</span></span>

### <span data-ttu-id="e5f6e-111">-Bild</span><span class="sxs-lookup"><span data-stu-id="e5f6e-111">-Image</span></span>
<span data-ttu-id="e5f6e-112">Gibt ein lokales Image-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="e5f6e-112">Specifies a local image object.</span></span>

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

### <span data-ttu-id="e5f6e-113">-Bildname</span><span class="sxs-lookup"><span data-stu-id="e5f6e-113">-ImageName</span></span>
<span data-ttu-id="e5f6e-114">Gibt den Namen eines Bilds an.</span><span class="sxs-lookup"><span data-stu-id="e5f6e-114">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="e5f6e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5f6e-115">-ResourceGroupName</span></span>
<span data-ttu-id="e5f6e-116">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="e5f6e-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e5f6e-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e5f6e-117">-Confirm</span></span>
<span data-ttu-id="e5f6e-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e5f6e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5f6e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5f6e-119">-WhatIf</span></span>
<span data-ttu-id="e5f6e-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e5f6e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5f6e-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e5f6e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5f6e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5f6e-122">CommonParameters</span></span>
<span data-ttu-id="e5f6e-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5f6e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5f6e-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5f6e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5f6e-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e5f6e-125">INPUTS</span></span>

### <span data-ttu-id="e5f6e-126">System. String</span><span class="sxs-lookup"><span data-stu-id="e5f6e-126">System.String</span></span>
<span data-ttu-id="e5f6e-127">Microsoft. Azure. Management. Compute. Models. Image</span><span class="sxs-lookup"><span data-stu-id="e5f6e-127">Microsoft.Azure.Management.Compute.Models.Image</span></span>

## <span data-ttu-id="e5f6e-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e5f6e-128">OUTPUTS</span></span>

### <span data-ttu-id="e5f6e-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="e5f6e-129">System.Object</span></span>

## <span data-ttu-id="e5f6e-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="e5f6e-130">NOTES</span></span>

## <span data-ttu-id="e5f6e-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e5f6e-131">RELATED LINKS</span></span>

