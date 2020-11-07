---
external help file: Azs.Gallery.Admin-help.xml
Module Name: Azs.Gallery.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 148cfa9db340b4a10e02b0870fc2edb5efb20a9a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661963"
---
# <span data-ttu-id="ec882-101">Remove-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="ec882-101">Remove-AzsGalleryItem</span></span>

## <span data-ttu-id="ec882-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ec882-102">SYNOPSIS</span></span>
<span data-ttu-id="ec882-103">Löschen eines bestimmten Katalogelements</span><span class="sxs-lookup"><span data-stu-id="ec882-103">Delete a specific gallery item.</span></span>

## <span data-ttu-id="ec882-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec882-104">SYNTAX</span></span>

### <span data-ttu-id="ec882-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="ec882-105">Delete (Default)</span></span>
```
Remove-AzsGalleryItem [-Name] <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec882-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec882-106">ResourceId</span></span>
```
Remove-AzsGalleryItem -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec882-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ec882-107">DESCRIPTION</span></span>
<span data-ttu-id="ec882-108">Löschen eines bestimmten Katalogelements</span><span class="sxs-lookup"><span data-stu-id="ec882-108">Delete a specific gallery item.</span></span>

## <span data-ttu-id="ec882-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ec882-109">EXAMPLES</span></span>

### <span data-ttu-id="ec882-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ec882-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsGalleryItem -Name "microsoft.vmss.1.3.6"
```

<span data-ttu-id="ec882-111">Löschen eines Katalogelements</span><span class="sxs-lookup"><span data-stu-id="ec882-111">Delete a gallery item.</span></span>

## <span data-ttu-id="ec882-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec882-112">PARAMETERS</span></span>

### <span data-ttu-id="ec882-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ec882-113">-Force</span></span>
<span data-ttu-id="ec882-114">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="ec882-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="ec882-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ec882-115">-Name</span></span>
<span data-ttu-id="ec882-116">Die Identität des Katalogelements.</span><span class="sxs-lookup"><span data-stu-id="ec882-116">Identity of the gallery item.</span></span>
<span data-ttu-id="ec882-117">Enthält den Namen des Herausgebers, den Elementnamen und kann die durch das Perioden Zeichen getrennte Version enthalten.</span><span class="sxs-lookup"><span data-stu-id="ec882-117">Includes publisher name, item name, and may include version separated by period character.</span></span>

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

### <span data-ttu-id="ec882-118">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ec882-118">-ResourceId</span></span>
<span data-ttu-id="ec882-119">Vollqualifizierte Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="ec882-119">Fully qualified Azure resource Id.</span></span>

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

### <span data-ttu-id="ec882-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ec882-120">-Confirm</span></span>
<span data-ttu-id="ec882-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ec882-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec882-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec882-122">-WhatIf</span></span>
<span data-ttu-id="ec882-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ec882-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec882-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ec882-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec882-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec882-125">CommonParameters</span></span>
<span data-ttu-id="ec882-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec882-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec882-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec882-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec882-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ec882-128">INPUTS</span></span>

## <span data-ttu-id="ec882-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ec882-129">OUTPUTS</span></span>

## <span data-ttu-id="ec882-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="ec882-130">NOTES</span></span>

## <span data-ttu-id="ec882-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ec882-131">RELATED LINKS</span></span>

