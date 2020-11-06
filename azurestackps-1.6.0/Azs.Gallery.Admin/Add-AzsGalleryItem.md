---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: db1f78f3adec999cdf8839eb972a71595f6c15b5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475269"
---
# <span data-ttu-id="9a9b9-101">Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="9a9b9-101">Add-AzsGalleryItem</span></span>

## <span data-ttu-id="9a9b9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9a9b9-102">SYNOPSIS</span></span>
<span data-ttu-id="9a9b9-103">Lädt ein Anbieter Katalogelement in den Speicher hoch.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-103">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="9a9b9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a9b9-104">SYNTAX</span></span>

```
Add-AzsGalleryItem [-GalleryItemUri] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a9b9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9a9b9-105">DESCRIPTION</span></span>
<span data-ttu-id="9a9b9-106">Lädt ein Anbieter Katalogelement in den Speicher hoch.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-106">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="9a9b9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9a9b9-107">EXAMPLES</span></span>

### <span data-ttu-id="9a9b9-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9a9b9-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsGalleryItem -GalleryItemUri 'http://galleryitemuri'
```

<span data-ttu-id="9a9b9-109">Erstellen eines neuen Katalogelements</span><span class="sxs-lookup"><span data-stu-id="9a9b9-109">Create a new gallery item.</span></span>

## <span data-ttu-id="9a9b9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a9b9-110">PARAMETERS</span></span>

### <span data-ttu-id="9a9b9-111">-Force</span><span class="sxs-lookup"><span data-stu-id="9a9b9-111">-Force</span></span>
<span data-ttu-id="9a9b9-112">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-112">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="9a9b9-113">-GalleryItemUri</span><span class="sxs-lookup"><span data-stu-id="9a9b9-113">-GalleryItemUri</span></span>
<span data-ttu-id="9a9b9-114">Der URI für die JSON-Datei des Katalogelements.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-114">The URI to the gallery item JSON file.</span></span>

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

### <span data-ttu-id="9a9b9-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9a9b9-115">-Confirm</span></span>
<span data-ttu-id="9a9b9-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a9b9-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a9b9-117">-WhatIf</span></span>
<span data-ttu-id="9a9b9-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a9b9-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a9b9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a9b9-120">CommonParameters</span></span>
<span data-ttu-id="9a9b9-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a9b9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a9b9-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a9b9-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a9b9-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9a9b9-123">INPUTS</span></span>

## <span data-ttu-id="9a9b9-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9a9b9-124">OUTPUTS</span></span>

### <span data-ttu-id="9a9b9-125">Microsoft. AzureStack. Management. Gallery. admin. Models. GalleryItem</span><span class="sxs-lookup"><span data-stu-id="9a9b9-125">Microsoft.AzureStack.Management.Gallery.Admin.Models.GalleryItem</span></span>

## <span data-ttu-id="9a9b9-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="9a9b9-126">NOTES</span></span>

## <span data-ttu-id="9a9b9-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9a9b9-127">RELATED LINKS</span></span>

