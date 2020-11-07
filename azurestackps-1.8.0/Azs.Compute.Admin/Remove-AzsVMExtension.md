---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0aa30655a7fa73b6cb53de12f8906ebb59ea5a17
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827636"
---
# <span data-ttu-id="5a7bf-101">Remove-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="5a7bf-101">Remove-AzsVMExtension</span></span>

## <span data-ttu-id="5a7bf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5a7bf-102">SYNOPSIS</span></span>
<span data-ttu-id="5a7bf-103">Löscht ein Abbild einer virtuellen Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="5a7bf-103">Deletes a virtual machine extension image.</span></span>

## <span data-ttu-id="5a7bf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a7bf-104">SYNTAX</span></span>

### <span data-ttu-id="5a7bf-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="5a7bf-105">Delete (Default)</span></span>
```
Remove-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a7bf-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a7bf-106">ResourceId</span></span>
```
Remove-AzsVMExtension -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a7bf-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5a7bf-107">DESCRIPTION</span></span>
<span data-ttu-id="5a7bf-108">Löscht das angegebene Image der virtuellen Computererweiterung.</span><span class="sxs-lookup"><span data-stu-id="5a7bf-108">Deletes specified virtual machine extension image.</span></span>

## <span data-ttu-id="5a7bf-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5a7bf-109">EXAMPLES</span></span>

### <span data-ttu-id="5a7bf-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5a7bf-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsVMExtension -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0"
```

<span data-ttu-id="5a7bf-111">Entfernen einer Plattform-Bild Erweiterung</span><span class="sxs-lookup"><span data-stu-id="5a7bf-111">Remove a platform image extension.</span></span>

## <span data-ttu-id="5a7bf-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a7bf-112">PARAMETERS</span></span>

### <span data-ttu-id="5a7bf-113">-Force</span><span class="sxs-lookup"><span data-stu-id="5a7bf-113">-Force</span></span>
<span data-ttu-id="5a7bf-114">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="5a7bf-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="5a7bf-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="5a7bf-115">-Location</span></span>
<span data-ttu-id="5a7bf-116">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="5a7bf-116">Location of the resource.</span></span>

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

### <span data-ttu-id="5a7bf-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="5a7bf-117">-Publisher</span></span>
<span data-ttu-id="5a7bf-118">Der Name des Herausgebers.</span><span class="sxs-lookup"><span data-stu-id="5a7bf-118">Name of the publisher.</span></span>

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

### <span data-ttu-id="5a7bf-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5a7bf-119">-ResourceId</span></span>
<span data-ttu-id="5a7bf-120">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="5a7bf-120">The resource id.</span></span>

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

### <span data-ttu-id="5a7bf-121">-Typ</span><span class="sxs-lookup"><span data-stu-id="5a7bf-121">-Type</span></span>
<span data-ttu-id="5a7bf-122">Der Typ der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="5a7bf-122">Type of extension.</span></span>

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

### <span data-ttu-id="5a7bf-123">-Version</span><span class="sxs-lookup"><span data-stu-id="5a7bf-123">-Version</span></span>
<span data-ttu-id="5a7bf-124">Die Version des Image der Virtual Machine-Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="5a7bf-124">The version of the virtual machine extension image.</span></span>

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

### <span data-ttu-id="5a7bf-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5a7bf-125">-Confirm</span></span>
<span data-ttu-id="5a7bf-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5a7bf-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a7bf-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a7bf-127">-WhatIf</span></span>
<span data-ttu-id="5a7bf-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5a7bf-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a7bf-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5a7bf-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a7bf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a7bf-130">CommonParameters</span></span>
<span data-ttu-id="5a7bf-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a7bf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a7bf-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a7bf-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a7bf-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5a7bf-133">INPUTS</span></span>

## <span data-ttu-id="5a7bf-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5a7bf-134">OUTPUTS</span></span>

## <span data-ttu-id="5a7bf-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="5a7bf-135">NOTES</span></span>

## <span data-ttu-id="5a7bf-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5a7bf-136">RELATED LINKS</span></span>

