---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 869cd48507ba9384026f8e58b9cd7853179b844f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475473"
---
# <span data-ttu-id="c5c3b-101">Get-AzsScaleUnit</span><span class="sxs-lookup"><span data-stu-id="c5c3b-101">Get-AzsScaleUnit</span></span>

## <span data-ttu-id="c5c3b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c5c3b-102">SYNOPSIS</span></span>
<span data-ttu-id="c5c3b-103">Gibt eine Liste aller Skaleneinheiten an einer Position zurück.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-103">Returns a list of all scale units at a location.</span></span>

## <span data-ttu-id="c5c3b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5c3b-104">SYNTAX</span></span>

### <span data-ttu-id="c5c3b-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="c5c3b-105">List (Default)</span></span>
```
Get-AzsScaleUnit [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="c5c3b-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="c5c3b-106">Get</span></span>
```
Get-AzsScaleUnit [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="c5c3b-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5c3b-107">ResourceId</span></span>
```
Get-AzsScaleUnit -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="c5c3b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c5c3b-108">DESCRIPTION</span></span>
<span data-ttu-id="c5c3b-109">Gibt eine Liste aller Skaleneinheiten an einer Position zurück.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-109">Returns a list of all scale units at a location.</span></span>

## <span data-ttu-id="c5c3b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c5c3b-110">EXAMPLES</span></span>

### <span data-ttu-id="c5c3b-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c5c3b-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsScaleUnit
```

<span data-ttu-id="c5c3b-112">Geben Sie eine Liste mit Informationen zu Skaleneinheiten zurück.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-112">Return a list of information about scale units.</span></span>

### <span data-ttu-id="c5c3b-113">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="c5c3b-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsScaleUnit -Name "S-Cluster"
```

<span data-ttu-id="c5c3b-114">Gibt Informationen zu einer bestimmten Skalierungseinheit zurück.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-114">Return information about a specific scale unit.</span></span>

## <span data-ttu-id="c5c3b-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5c3b-115">PARAMETERS</span></span>

### <span data-ttu-id="c5c3b-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="c5c3b-116">-Filter</span></span>
<span data-ttu-id="c5c3b-117">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="c5c3b-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="c5c3b-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="c5c3b-118">-Location</span></span>
<span data-ttu-id="c5c3b-119">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-119">Location of the resource.</span></span>

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

### <span data-ttu-id="c5c3b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c5c3b-120">-Name</span></span>
<span data-ttu-id="c5c3b-121">Name der Skalierungseinheiten</span><span class="sxs-lookup"><span data-stu-id="c5c3b-121">Name of the scale units.</span></span>

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

### <span data-ttu-id="c5c3b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5c3b-122">-ResourceGroupName</span></span>
<span data-ttu-id="c5c3b-123">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="c5c3b-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c5c3b-124">-ResourceId</span></span>
<span data-ttu-id="c5c3b-125">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-125">The resource id.</span></span>

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

### <span data-ttu-id="c5c3b-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="c5c3b-126">-Skip</span></span>
<span data-ttu-id="c5c3b-127">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="c5c3b-128">-Top</span><span class="sxs-lookup"><span data-stu-id="c5c3b-128">-Top</span></span>
<span data-ttu-id="c5c3b-129">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="c5c3b-130">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="c5c3b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5c3b-131">CommonParameters</span></span>
<span data-ttu-id="c5c3b-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5c3b-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5c3b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5c3b-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c5c3b-134">INPUTS</span></span>

## <span data-ttu-id="c5c3b-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c5c3b-135">OUTPUTS</span></span>

### <span data-ttu-id="c5c3b-136">Microsoft. AzureStack. Management. Fabric. admin. Models. ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="c5c3b-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.ScaleUnit</span></span>

## <span data-ttu-id="c5c3b-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="c5c3b-137">NOTES</span></span>

## <span data-ttu-id="c5c3b-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c5c3b-138">RELATED LINKS</span></span>

