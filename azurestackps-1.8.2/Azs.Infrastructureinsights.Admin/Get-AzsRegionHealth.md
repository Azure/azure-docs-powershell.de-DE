---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2d07aad989b08909228aebca7538b007f36bfcab
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007316"
---
# <span data-ttu-id="9953e-101">Get-AzsRegionHealth</span><span class="sxs-lookup"><span data-stu-id="9953e-101">Get-AzsRegionHealth</span></span>

## <span data-ttu-id="9953e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9953e-102">SYNOPSIS</span></span>
<span data-ttu-id="9953e-103">Gibt eine Liste des Gesundheitszustands des Bereichs zurück.</span><span class="sxs-lookup"><span data-stu-id="9953e-103">Returns a list of region's health status.</span></span>

## <span data-ttu-id="9953e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9953e-104">SYNTAX</span></span>

### <span data-ttu-id="9953e-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="9953e-105">List (Default)</span></span>
```
Get-AzsRegionHealth [-ResourceGroupName <String>] [-Filter <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="9953e-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="9953e-106">Get</span></span>
```
Get-AzsRegionHealth [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="9953e-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9953e-107">ResourceId</span></span>
```
Get-AzsRegionHealth -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="9953e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9953e-108">DESCRIPTION</span></span>
<span data-ttu-id="9953e-109">Gibt eine Liste des Gesundheitszustands des Bereichs zurück.</span><span class="sxs-lookup"><span data-stu-id="9953e-109">Returns a list of region's health status.</span></span>

## <span data-ttu-id="9953e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9953e-110">EXAMPLES</span></span>

### <span data-ttu-id="9953e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9953e-111">EXAMPLE 1</span></span>
```
Get-AzsRegionHealth
```

<span data-ttu-id="9953e-112">Gibt eine Liste des Gesundheitszustands des Bereichs zurück.</span><span class="sxs-lookup"><span data-stu-id="9953e-112">Returns a list of region's health status.</span></span>

## <span data-ttu-id="9953e-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="9953e-113">PARAMETERS</span></span>

### <span data-ttu-id="9953e-114">-Standort</span><span class="sxs-lookup"><span data-stu-id="9953e-114">-Location</span></span>
<span data-ttu-id="9953e-115">Name der Region</span><span class="sxs-lookup"><span data-stu-id="9953e-115">Name of the region</span></span>

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

### <span data-ttu-id="9953e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9953e-116">-ResourceGroupName</span></span>
<span data-ttu-id="9953e-117">Ressourcengruppenname, optional.</span><span class="sxs-lookup"><span data-stu-id="9953e-117">Resource group name, optional.</span></span>

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

### <span data-ttu-id="9953e-118">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="9953e-118">-ResourceId</span></span>
<span data-ttu-id="9953e-119">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="9953e-119">The resource id.</span></span>

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

### <span data-ttu-id="9953e-120">-Filter</span><span class="sxs-lookup"><span data-stu-id="9953e-120">-Filter</span></span>
<span data-ttu-id="9953e-121">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="9953e-121">OData filter parameter.</span></span>

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

### <span data-ttu-id="9953e-122">-Top</span><span class="sxs-lookup"><span data-stu-id="9953e-122">-Top</span></span>
<span data-ttu-id="9953e-123">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="9953e-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="9953e-124">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="9953e-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="9953e-125">-Skip</span><span class="sxs-lookup"><span data-stu-id="9953e-125">-Skip</span></span>
<span data-ttu-id="9953e-126">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="9953e-126">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="9953e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9953e-127">CommonParameters</span></span>
<span data-ttu-id="9953e-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9953e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9953e-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9953e-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9953e-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9953e-130">INPUTS</span></span>

## <span data-ttu-id="9953e-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9953e-131">OUTPUTS</span></span>

### <span data-ttu-id="9953e-132">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. RegionHealth</span><span class="sxs-lookup"><span data-stu-id="9953e-132">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.RegionHealth</span></span>

## <span data-ttu-id="9953e-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="9953e-133">NOTES</span></span>

## <span data-ttu-id="9953e-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9953e-134">RELATED LINKS</span></span>
