---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 947bb6b453d92897f7901a00ed5a43efa4ac640e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661893"
---
# <span data-ttu-id="f968f-101">Remove-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="f968f-101">Remove-AzsPlatformImage</span></span>

## <span data-ttu-id="f968f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f968f-102">SYNOPSIS</span></span>
<span data-ttu-id="f968f-103">Löschen Sie ein Bild eines virtuellen Computers aus dem Platform-Image-Repository.</span><span class="sxs-lookup"><span data-stu-id="f968f-103">Delete a virtual machine image from the platform image repository.</span></span>

## <span data-ttu-id="f968f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f968f-104">SYNTAX</span></span>

### <span data-ttu-id="f968f-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="f968f-105">Delete (Default)</span></span>
```
Remove-AzsPlatformImage -Publisher <String> -Offer <String> -Sku <String> -Version <String>
 [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f968f-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f968f-106">ResourceId</span></span>
```
Remove-AzsPlatformImage -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f968f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f968f-107">DESCRIPTION</span></span>
<span data-ttu-id="f968f-108">Löschen eines Platt Form Bilds</span><span class="sxs-lookup"><span data-stu-id="f968f-108">Delete a platform image</span></span>

## <span data-ttu-id="f968f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f968f-109">EXAMPLES</span></span>

### <span data-ttu-id="f968f-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f968f-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlatformImage -Publisher Test -Offer UbuntuServer -Version 1.0.0 -Sku 16.04-LTS
```

<span data-ttu-id="f968f-111">Löschen eines vorhandenen Platt Form Bilds</span><span class="sxs-lookup"><span data-stu-id="f968f-111">Delete an existing platform image.</span></span>

## <span data-ttu-id="f968f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f968f-112">PARAMETERS</span></span>

### <span data-ttu-id="f968f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="f968f-113">-Force</span></span>
<span data-ttu-id="f968f-114">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="f968f-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="f968f-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="f968f-115">-Location</span></span>
<span data-ttu-id="f968f-116">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="f968f-116">Location of the resource.</span></span>

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

### <span data-ttu-id="f968f-117">-Angebot</span><span class="sxs-lookup"><span data-stu-id="f968f-117">-Offer</span></span>
<span data-ttu-id="f968f-118">Name des Angebots.</span><span class="sxs-lookup"><span data-stu-id="f968f-118">Name of the offer.</span></span>

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

### <span data-ttu-id="f968f-119">-Publisher</span><span class="sxs-lookup"><span data-stu-id="f968f-119">-Publisher</span></span>
<span data-ttu-id="f968f-120">Der Name des Herausgebers.</span><span class="sxs-lookup"><span data-stu-id="f968f-120">Name of the publisher.</span></span>

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

### <span data-ttu-id="f968f-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f968f-121">-ResourceId</span></span>
<span data-ttu-id="f968f-122">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="f968f-122">The resource id.</span></span>

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

### <span data-ttu-id="f968f-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="f968f-123">-Sku</span></span>
<span data-ttu-id="f968f-124">Der Name der SKU.</span><span class="sxs-lookup"><span data-stu-id="f968f-124">Name of the SKU.</span></span>

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

### <span data-ttu-id="f968f-125">-Version</span><span class="sxs-lookup"><span data-stu-id="f968f-125">-Version</span></span>
<span data-ttu-id="f968f-126">Die Version des virtuellen Computer Bilds.</span><span class="sxs-lookup"><span data-stu-id="f968f-126">The version of the virtual machine image.</span></span>

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

### <span data-ttu-id="f968f-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f968f-127">-Confirm</span></span>
<span data-ttu-id="f968f-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f968f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f968f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f968f-129">-WhatIf</span></span>
<span data-ttu-id="f968f-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f968f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f968f-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f968f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f968f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f968f-132">CommonParameters</span></span>
<span data-ttu-id="f968f-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f968f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f968f-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f968f-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f968f-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f968f-135">INPUTS</span></span>

## <span data-ttu-id="f968f-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f968f-136">OUTPUTS</span></span>

## <span data-ttu-id="f968f-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="f968f-137">NOTES</span></span>

## <span data-ttu-id="f968f-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f968f-138">RELATED LINKS</span></span>

