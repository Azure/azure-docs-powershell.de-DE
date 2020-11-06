---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b6713b912f962a7a85627ca2280d6195cc5c5d88
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475010"
---
# <span data-ttu-id="49d2d-101">Get-AzsRegionHealth</span><span class="sxs-lookup"><span data-stu-id="49d2d-101">Get-AzsRegionHealth</span></span>

## <span data-ttu-id="49d2d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="49d2d-102">SYNOPSIS</span></span>
<span data-ttu-id="49d2d-103">Gibt eine Liste des Gesundheitszustands des Bereichs zurück.</span><span class="sxs-lookup"><span data-stu-id="49d2d-103">Returns a list of region's health status.</span></span>

## <span data-ttu-id="49d2d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="49d2d-104">SYNTAX</span></span>

### <span data-ttu-id="49d2d-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="49d2d-105">List (Default)</span></span>
```
Get-AzsRegionHealth [-ResourceGroupName <String>] [-Filter <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="49d2d-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="49d2d-106">Get</span></span>
```
Get-AzsRegionHealth [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="49d2d-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="49d2d-107">ResourceId</span></span>
```
Get-AzsRegionHealth -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="49d2d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="49d2d-108">DESCRIPTION</span></span>
<span data-ttu-id="49d2d-109">Gibt eine Liste des Gesundheitszustands des Bereichs zurück.</span><span class="sxs-lookup"><span data-stu-id="49d2d-109">Returns a list of region's health status.</span></span>

## <span data-ttu-id="49d2d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="49d2d-110">EXAMPLES</span></span>

### <span data-ttu-id="49d2d-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="49d2d-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsRegionHealth
```

<span data-ttu-id="49d2d-112">Gibt eine Liste des Gesundheitszustands des Bereichs zurück.</span><span class="sxs-lookup"><span data-stu-id="49d2d-112">Returns a list of region's health status.</span></span>

## <span data-ttu-id="49d2d-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="49d2d-113">PARAMETERS</span></span>

### <span data-ttu-id="49d2d-114">-Filter</span><span class="sxs-lookup"><span data-stu-id="49d2d-114">-Filter</span></span>
<span data-ttu-id="49d2d-115">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="49d2d-115">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49d2d-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="49d2d-116">-Location</span></span>
<span data-ttu-id="49d2d-117">Name der Region</span><span class="sxs-lookup"><span data-stu-id="49d2d-117">Name of the region</span></span>

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

### <span data-ttu-id="49d2d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49d2d-118">-ResourceGroupName</span></span>
<span data-ttu-id="49d2d-119">Der Ressourcengruppenname, in dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="49d2d-119">Resource group name which the resource resides.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49d2d-120">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="49d2d-120">-ResourceId</span></span>
<span data-ttu-id="49d2d-121">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="49d2d-121">The resource id.</span></span>

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

### <span data-ttu-id="49d2d-122">-Skip</span><span class="sxs-lookup"><span data-stu-id="49d2d-122">-Skip</span></span>
<span data-ttu-id="49d2d-123">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="49d2d-123">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49d2d-124">-Top</span><span class="sxs-lookup"><span data-stu-id="49d2d-124">-Top</span></span>
<span data-ttu-id="49d2d-125">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="49d2d-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="49d2d-126">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="49d2d-126">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49d2d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49d2d-127">CommonParameters</span></span>
<span data-ttu-id="49d2d-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49d2d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49d2d-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49d2d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49d2d-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="49d2d-130">INPUTS</span></span>

## <span data-ttu-id="49d2d-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="49d2d-131">OUTPUTS</span></span>

### <span data-ttu-id="49d2d-132">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. RegionHealth</span><span class="sxs-lookup"><span data-stu-id="49d2d-132">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.RegionHealth</span></span>

## <span data-ttu-id="49d2d-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="49d2d-133">NOTES</span></span>

## <span data-ttu-id="49d2d-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="49d2d-134">RELATED LINKS</span></span>

