---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2d07aad989b08909228aebca7538b007f36bfcab
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840763"
---
# <span data-ttu-id="6b1f2-101">Get-AzsRegionHealth</span><span class="sxs-lookup"><span data-stu-id="6b1f2-101">Get-AzsRegionHealth</span></span>

## <span data-ttu-id="6b1f2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6b1f2-102">SYNOPSIS</span></span>
<span data-ttu-id="6b1f2-103">Gibt eine Liste des Gesundheitszustands des Bereichs zurück.</span><span class="sxs-lookup"><span data-stu-id="6b1f2-103">Returns a list of region's health status.</span></span>

## <span data-ttu-id="6b1f2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b1f2-104">SYNTAX</span></span>

### <span data-ttu-id="6b1f2-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="6b1f2-105">List (Default)</span></span>
```
Get-AzsRegionHealth [-ResourceGroupName <String>] [-Filter <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="6b1f2-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="6b1f2-106">Get</span></span>
```
Get-AzsRegionHealth [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="6b1f2-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b1f2-107">ResourceId</span></span>
```
Get-AzsRegionHealth -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="6b1f2-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6b1f2-108">DESCRIPTION</span></span>
<span data-ttu-id="6b1f2-109">Gibt eine Liste des Gesundheitszustands des Bereichs zurück.</span><span class="sxs-lookup"><span data-stu-id="6b1f2-109">Returns a list of region's health status.</span></span>

## <span data-ttu-id="6b1f2-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6b1f2-110">EXAMPLES</span></span>

### <span data-ttu-id="6b1f2-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6b1f2-111">EXAMPLE 1</span></span>
```
Get-AzsRegionHealth
```

<span data-ttu-id="6b1f2-112">Gibt eine Liste des Gesundheitszustands des Bereichs zurück.</span><span class="sxs-lookup"><span data-stu-id="6b1f2-112">Returns a list of region's health status.</span></span>

## <span data-ttu-id="6b1f2-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b1f2-113">PARAMETERS</span></span>

### <span data-ttu-id="6b1f2-114">-Standort</span><span class="sxs-lookup"><span data-stu-id="6b1f2-114">-Location</span></span>
<span data-ttu-id="6b1f2-115">Name der Region</span><span class="sxs-lookup"><span data-stu-id="6b1f2-115">Name of the region</span></span>

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

### <span data-ttu-id="6b1f2-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b1f2-116">-ResourceGroupName</span></span>
<span data-ttu-id="6b1f2-117">Ressourcengruppenname, optional.</span><span class="sxs-lookup"><span data-stu-id="6b1f2-117">Resource group name, optional.</span></span>

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

### <span data-ttu-id="6b1f2-118">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="6b1f2-118">-ResourceId</span></span>
<span data-ttu-id="6b1f2-119">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="6b1f2-119">The resource id.</span></span>

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

### <span data-ttu-id="6b1f2-120">-Filter</span><span class="sxs-lookup"><span data-stu-id="6b1f2-120">-Filter</span></span>
<span data-ttu-id="6b1f2-121">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="6b1f2-121">OData filter parameter.</span></span>

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

### <span data-ttu-id="6b1f2-122">-Top</span><span class="sxs-lookup"><span data-stu-id="6b1f2-122">-Top</span></span>
<span data-ttu-id="6b1f2-123">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="6b1f2-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="6b1f2-124">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="6b1f2-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="6b1f2-125">-Skip</span><span class="sxs-lookup"><span data-stu-id="6b1f2-125">-Skip</span></span>
<span data-ttu-id="6b1f2-126">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="6b1f2-126">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="6b1f2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b1f2-127">CommonParameters</span></span>
<span data-ttu-id="6b1f2-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b1f2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b1f2-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b1f2-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b1f2-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6b1f2-130">INPUTS</span></span>

## <span data-ttu-id="6b1f2-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6b1f2-131">OUTPUTS</span></span>

### <span data-ttu-id="6b1f2-132">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. RegionHealth</span><span class="sxs-lookup"><span data-stu-id="6b1f2-132">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.RegionHealth</span></span>

## <span data-ttu-id="6b1f2-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="6b1f2-133">NOTES</span></span>

## <span data-ttu-id="6b1f2-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6b1f2-134">RELATED LINKS</span></span>
