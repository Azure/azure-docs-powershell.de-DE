---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 28d807ebcd1ae61844b0316492b3d9d10437f1d3
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827639"
---
# <span data-ttu-id="3fdca-101">Remove-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="3fdca-101">Remove-AzsPlatformImage</span></span>

## <span data-ttu-id="3fdca-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3fdca-102">SYNOPSIS</span></span>
<span data-ttu-id="3fdca-103">Löschen Sie ein Bild eines virtuellen Computers aus dem Platform-Image-Repository.</span><span class="sxs-lookup"><span data-stu-id="3fdca-103">Delete a virtual machine image from the platform image repository.</span></span>

## <span data-ttu-id="3fdca-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3fdca-104">SYNTAX</span></span>

### <span data-ttu-id="3fdca-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="3fdca-105">Delete (Default)</span></span>
```
Remove-AzsPlatformImage -Publisher <String> -Offer <String> -Sku <String> -Version <String>
 [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fdca-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="3fdca-106">ResourceId</span></span>
```
Remove-AzsPlatformImage -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fdca-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3fdca-107">DESCRIPTION</span></span>
<span data-ttu-id="3fdca-108">Löschen eines Platt Form Bilds</span><span class="sxs-lookup"><span data-stu-id="3fdca-108">Delete a platform image</span></span>

## <span data-ttu-id="3fdca-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3fdca-109">EXAMPLES</span></span>

### <span data-ttu-id="3fdca-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3fdca-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlatformImage -Publisher Test -Offer UbuntuServer -Version 1.0.0 -Sku 16.04-LTS
```

<span data-ttu-id="3fdca-111">Löschen eines vorhandenen Platt Form Bilds</span><span class="sxs-lookup"><span data-stu-id="3fdca-111">Delete an existing platform image.</span></span>

## <span data-ttu-id="3fdca-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="3fdca-112">PARAMETERS</span></span>

### <span data-ttu-id="3fdca-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3fdca-113">-Force</span></span>
<span data-ttu-id="3fdca-114">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="3fdca-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="3fdca-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="3fdca-115">-Location</span></span>
<span data-ttu-id="3fdca-116">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="3fdca-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fdca-117">-Angebot</span><span class="sxs-lookup"><span data-stu-id="3fdca-117">-Offer</span></span>
<span data-ttu-id="3fdca-118">Name des Angebots.</span><span class="sxs-lookup"><span data-stu-id="3fdca-118">Name of the offer.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fdca-119">-Publisher</span><span class="sxs-lookup"><span data-stu-id="3fdca-119">-Publisher</span></span>
<span data-ttu-id="3fdca-120">Der Name des Herausgebers.</span><span class="sxs-lookup"><span data-stu-id="3fdca-120">Name of the publisher.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fdca-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3fdca-121">-ResourceId</span></span>
<span data-ttu-id="3fdca-122">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="3fdca-122">The resource id.</span></span>

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

### <span data-ttu-id="3fdca-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="3fdca-123">-Sku</span></span>
<span data-ttu-id="3fdca-124">Der Name der SKU.</span><span class="sxs-lookup"><span data-stu-id="3fdca-124">Name of the SKU.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fdca-125">-Version</span><span class="sxs-lookup"><span data-stu-id="3fdca-125">-Version</span></span>
<span data-ttu-id="3fdca-126">Die Version des virtuellen Computer Bilds.</span><span class="sxs-lookup"><span data-stu-id="3fdca-126">The version of the virtual machine image.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fdca-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3fdca-127">-Confirm</span></span>
<span data-ttu-id="3fdca-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3fdca-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fdca-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fdca-129">-WhatIf</span></span>
<span data-ttu-id="3fdca-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3fdca-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fdca-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3fdca-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fdca-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fdca-132">CommonParameters</span></span>
<span data-ttu-id="3fdca-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fdca-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fdca-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fdca-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fdca-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3fdca-135">INPUTS</span></span>

## <span data-ttu-id="3fdca-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3fdca-136">OUTPUTS</span></span>

## <span data-ttu-id="3fdca-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="3fdca-137">NOTES</span></span>

## <span data-ttu-id="3fdca-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3fdca-138">RELATED LINKS</span></span>

