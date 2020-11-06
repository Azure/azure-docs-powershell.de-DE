---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2f87690c20357cbff7f85a405dd6d3fae3a72dc9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93474926"
---
# <span data-ttu-id="ea70c-101">Remove-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="ea70c-101">Remove-AzsVMExtension</span></span>

## <span data-ttu-id="ea70c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ea70c-102">SYNOPSIS</span></span>
<span data-ttu-id="ea70c-103">Löscht ein Abbild einer virtuellen Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="ea70c-103">Deletes a virtual machine extension image.</span></span>

## <span data-ttu-id="ea70c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea70c-104">SYNTAX</span></span>

### <span data-ttu-id="ea70c-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="ea70c-105">Delete (Default)</span></span>
```
Remove-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea70c-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea70c-106">ResourceId</span></span>
```
Remove-AzsVMExtension -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea70c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ea70c-107">DESCRIPTION</span></span>
<span data-ttu-id="ea70c-108">Löscht das angegebene Image der virtuellen Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="ea70c-108">Deletes specified virtual machine extension image.</span></span>

## <span data-ttu-id="ea70c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ea70c-109">EXAMPLES</span></span>

### <span data-ttu-id="ea70c-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ea70c-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0"
```

<span data-ttu-id="ea70c-111">Entfernen einer Plattform-Bild Erweiterung</span><span class="sxs-lookup"><span data-stu-id="ea70c-111">Remove a platform image extension.</span></span>

## <span data-ttu-id="ea70c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea70c-112">PARAMETERS</span></span>

### <span data-ttu-id="ea70c-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ea70c-113">-Force</span></span>
<span data-ttu-id="ea70c-114">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="ea70c-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="ea70c-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="ea70c-115">-Location</span></span>
<span data-ttu-id="ea70c-116">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="ea70c-116">Location of the resource.</span></span>

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

### <span data-ttu-id="ea70c-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="ea70c-117">-Publisher</span></span>
<span data-ttu-id="ea70c-118">Der Name des Herausgebers.</span><span class="sxs-lookup"><span data-stu-id="ea70c-118">Name of the publisher.</span></span>

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

### <span data-ttu-id="ea70c-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ea70c-119">-ResourceId</span></span>
<span data-ttu-id="ea70c-120">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="ea70c-120">The resource id.</span></span>

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

### <span data-ttu-id="ea70c-121">-Typ</span><span class="sxs-lookup"><span data-stu-id="ea70c-121">-Type</span></span>
<span data-ttu-id="ea70c-122">Der Typ der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="ea70c-122">Type of extension.</span></span>

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

### <span data-ttu-id="ea70c-123">-Version</span><span class="sxs-lookup"><span data-stu-id="ea70c-123">-Version</span></span>
<span data-ttu-id="ea70c-124">Die Version des Image der Virtual Machine-Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="ea70c-124">The version of the virtual machine extension image.</span></span>

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

### <span data-ttu-id="ea70c-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ea70c-125">-Confirm</span></span>
<span data-ttu-id="ea70c-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ea70c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea70c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea70c-127">-WhatIf</span></span>
<span data-ttu-id="ea70c-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ea70c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea70c-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ea70c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea70c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea70c-130">CommonParameters</span></span>
<span data-ttu-id="ea70c-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea70c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea70c-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea70c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea70c-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ea70c-133">INPUTS</span></span>

## <span data-ttu-id="ea70c-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ea70c-134">OUTPUTS</span></span>

## <span data-ttu-id="ea70c-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="ea70c-135">NOTES</span></span>

## <span data-ttu-id="ea70c-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ea70c-136">RELATED LINKS</span></span>

