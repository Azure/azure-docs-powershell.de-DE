---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8fc33149fa47c6c70207bebfe87e554fe7eb60cf
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007344"
---
# <span data-ttu-id="e8f55-101">Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="e8f55-101">Remove-AzsGalleryItem</span></span>

## <span data-ttu-id="e8f55-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e8f55-102">SYNOPSIS</span></span>
<span data-ttu-id="e8f55-103">Löschen eines bestimmten Katalogelements</span><span class="sxs-lookup"><span data-stu-id="e8f55-103">Delete a specific gallery item.</span></span>

## <span data-ttu-id="e8f55-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8f55-104">SYNTAX</span></span>

### <span data-ttu-id="e8f55-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="e8f55-105">Delete (Default)</span></span>
```
Remove-AzsGalleryItem [-Name] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8f55-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8f55-106">ResourceId</span></span>
```
Remove-AzsGalleryItem -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8f55-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e8f55-107">DESCRIPTION</span></span>
<span data-ttu-id="e8f55-108">Löschen eines bestimmten Katalogelements</span><span class="sxs-lookup"><span data-stu-id="e8f55-108">Delete a specific gallery item.</span></span>

## <span data-ttu-id="e8f55-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e8f55-109">EXAMPLES</span></span>

### <span data-ttu-id="e8f55-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e8f55-110">EXAMPLE 1</span></span>
```
Remove-AzsGalleryItem -Name "microsoft.vmss.1.3.6"
```

<span data-ttu-id="e8f55-111">Löschen eines Katalogelements</span><span class="sxs-lookup"><span data-stu-id="e8f55-111">Delete a gallery item.</span></span>

## <span data-ttu-id="e8f55-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8f55-112">PARAMETERS</span></span>

### <span data-ttu-id="e8f55-113">-Name</span><span class="sxs-lookup"><span data-stu-id="e8f55-113">-Name</span></span>
<span data-ttu-id="e8f55-114">Die Identität des Katalogelements.</span><span class="sxs-lookup"><span data-stu-id="e8f55-114">Identity of the gallery item.</span></span>
<span data-ttu-id="e8f55-115">Enthält den Namen des Herausgebers, den Elementnamen und kann die durch das Perioden Zeichen getrennte Version enthalten.</span><span class="sxs-lookup"><span data-stu-id="e8f55-115">Includes publisher name, item name, and may include version separated by period character.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8f55-116">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e8f55-116">-ResourceId</span></span>
<span data-ttu-id="e8f55-117">Vollqualifizierte Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="e8f55-117">Fully qualified Azure resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8f55-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e8f55-118">-Force</span></span>
<span data-ttu-id="e8f55-119">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="e8f55-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="e8f55-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8f55-120">-WhatIf</span></span>
<span data-ttu-id="e8f55-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e8f55-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8f55-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e8f55-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8f55-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e8f55-123">-Confirm</span></span>
<span data-ttu-id="e8f55-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e8f55-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8f55-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8f55-125">CommonParameters</span></span>
<span data-ttu-id="e8f55-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8f55-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8f55-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8f55-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8f55-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e8f55-128">INPUTS</span></span>

## <span data-ttu-id="e8f55-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e8f55-129">OUTPUTS</span></span>

## <span data-ttu-id="e8f55-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="e8f55-130">NOTES</span></span>

## <span data-ttu-id="e8f55-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e8f55-131">RELATED LINKS</span></span>
