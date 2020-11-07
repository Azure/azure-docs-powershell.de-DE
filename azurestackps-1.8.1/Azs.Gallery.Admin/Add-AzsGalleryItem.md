---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f0eadd6f0561ca5b44a588397f46d6ad3d7a1c3c
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840880"
---
# <span data-ttu-id="25d1d-101">Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="25d1d-101">Add-AzsGalleryItem</span></span>

## <span data-ttu-id="25d1d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="25d1d-102">SYNOPSIS</span></span>
<span data-ttu-id="25d1d-103">Lädt ein Anbieter Katalogelement in den Speicher hoch.</span><span class="sxs-lookup"><span data-stu-id="25d1d-103">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="25d1d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="25d1d-104">SYNTAX</span></span>

```
Add-AzsGalleryItem [-GalleryItemUri] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25d1d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="25d1d-105">DESCRIPTION</span></span>
<span data-ttu-id="25d1d-106">Lädt ein Anbieter Katalogelement in den Speicher hoch.</span><span class="sxs-lookup"><span data-stu-id="25d1d-106">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="25d1d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="25d1d-107">EXAMPLES</span></span>

### <span data-ttu-id="25d1d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="25d1d-108">EXAMPLE 1</span></span>
```
Add-AzsGalleryItem -GalleryItemUri 'http://galleryitemuri'
```

<span data-ttu-id="25d1d-109">Erstellen eines neuen Katalogelements</span><span class="sxs-lookup"><span data-stu-id="25d1d-109">Create a new gallery item.</span></span>

## <span data-ttu-id="25d1d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="25d1d-110">PARAMETERS</span></span>

### <span data-ttu-id="25d1d-111">-GalleryItemUri</span><span class="sxs-lookup"><span data-stu-id="25d1d-111">-GalleryItemUri</span></span>
<span data-ttu-id="25d1d-112">Der URI für die JSON-Datei des Katalogelements.</span><span class="sxs-lookup"><span data-stu-id="25d1d-112">The URI to the gallery item JSON file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25d1d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="25d1d-113">-Force</span></span>
<span data-ttu-id="25d1d-114">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="25d1d-114">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25d1d-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25d1d-115">-WhatIf</span></span>
<span data-ttu-id="25d1d-116">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="25d1d-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25d1d-117">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="25d1d-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25d1d-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="25d1d-118">-Confirm</span></span>
<span data-ttu-id="25d1d-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="25d1d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25d1d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25d1d-120">CommonParameters</span></span>
<span data-ttu-id="25d1d-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25d1d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25d1d-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25d1d-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25d1d-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="25d1d-123">INPUTS</span></span>

## <span data-ttu-id="25d1d-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="25d1d-124">OUTPUTS</span></span>

### <span data-ttu-id="25d1d-125">Microsoft. AzureStack. Management. Gallery. admin. Models. GalleryItem</span><span class="sxs-lookup"><span data-stu-id="25d1d-125">Microsoft.AzureStack.Management.Gallery.Admin.Models.GalleryItem</span></span>

## <span data-ttu-id="25d1d-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="25d1d-126">NOTES</span></span>

## <span data-ttu-id="25d1d-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="25d1d-127">RELATED LINKS</span></span>
