---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2020caba1d7cac4ed1830fbc1b6a3ccdb4c71f27
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475025"
---
# <span data-ttu-id="9ac7d-101">Get-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="9ac7d-101">Get-AzsGalleryItem</span></span>

## <span data-ttu-id="9ac7d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9ac7d-102">SYNOPSIS</span></span>
<span data-ttu-id="9ac7d-103">Listet Katalogelemente auf.</span><span class="sxs-lookup"><span data-stu-id="9ac7d-103">Lists gallery items.</span></span>

## <span data-ttu-id="9ac7d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ac7d-104">SYNTAX</span></span>

### <span data-ttu-id="9ac7d-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="9ac7d-105">List (Default)</span></span>
```
Get-AzsGalleryItem [<CommonParameters>]
```

### <span data-ttu-id="9ac7d-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="9ac7d-106">Get</span></span>
```
Get-AzsGalleryItem [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="9ac7d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9ac7d-107">DESCRIPTION</span></span>
<span data-ttu-id="9ac7d-108">Abrufen einer Liste der im Azure Stack Marketplace verfügbaren Katalogelemente</span><span class="sxs-lookup"><span data-stu-id="9ac7d-108">Get a list of gallery items available in Azure Stack Marketplace</span></span>

## <span data-ttu-id="9ac7d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9ac7d-109">EXAMPLES</span></span>

### <span data-ttu-id="9ac7d-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9ac7d-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsGalleryItem
```

<span data-ttu-id="9ac7d-111">Katalogelemente auflisten.</span><span class="sxs-lookup"><span data-stu-id="9ac7d-111">List gallery items.</span></span>

### <span data-ttu-id="9ac7d-112">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="9ac7d-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsGalleryItem -Name 'microsoft.vmss.1.3.6'
```

<span data-ttu-id="9ac7d-113">Besorgen Sie sich ein Katalogelement mit dem Namen.</span><span class="sxs-lookup"><span data-stu-id="9ac7d-113">Get a gallery item by name.</span></span>

## <span data-ttu-id="9ac7d-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ac7d-114">PARAMETERS</span></span>

### <span data-ttu-id="9ac7d-115">-Name</span><span class="sxs-lookup"><span data-stu-id="9ac7d-115">-Name</span></span>
<span data-ttu-id="9ac7d-116">Die Identität des Katalogelements.</span><span class="sxs-lookup"><span data-stu-id="9ac7d-116">Identity of the gallery item.</span></span>
<span data-ttu-id="9ac7d-117">Enthält den Namen des Herausgebers, den Elementnamen und kann die durch das Perioden Zeichen getrennte Version enthalten.</span><span class="sxs-lookup"><span data-stu-id="9ac7d-117">Includes publisher name, item name, and may include version separated by period character.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ac7d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ac7d-118">CommonParameters</span></span>
<span data-ttu-id="9ac7d-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ac7d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ac7d-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ac7d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ac7d-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9ac7d-121">INPUTS</span></span>

## <span data-ttu-id="9ac7d-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9ac7d-122">OUTPUTS</span></span>

### <span data-ttu-id="9ac7d-123">Microsoft. AzureStack. Management. Gallery. admin. Models. GalleryItem</span><span class="sxs-lookup"><span data-stu-id="9ac7d-123">Microsoft.AzureStack.Management.Gallery.Admin.Models.GalleryItem</span></span>

## <span data-ttu-id="9ac7d-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="9ac7d-124">NOTES</span></span>

## <span data-ttu-id="9ac7d-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9ac7d-125">RELATED LINKS</span></span>

