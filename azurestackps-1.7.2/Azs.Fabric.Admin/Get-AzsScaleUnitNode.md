---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d5870624b6d39b3e821ed6a7fb76d87c8422ab2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826624"
---
# <span data-ttu-id="9224e-101">Get-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="9224e-101">Get-AzsScaleUnitNode</span></span>

## <span data-ttu-id="9224e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9224e-102">SYNOPSIS</span></span>
<span data-ttu-id="9224e-103">Gibt eine Liste aller Skalierungseinheiten Knoten an einer Position zurück.</span><span class="sxs-lookup"><span data-stu-id="9224e-103">Returns a list of all scale unit nodes in a location.</span></span>

## <span data-ttu-id="9224e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9224e-104">SYNTAX</span></span>

### <span data-ttu-id="9224e-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="9224e-105">List (Default)</span></span>
```
Get-AzsScaleUnitNode [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="9224e-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="9224e-106">Get</span></span>
```
Get-AzsScaleUnitNode [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="9224e-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9224e-107">ResourceId</span></span>
```
Get-AzsScaleUnitNode -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="9224e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9224e-108">DESCRIPTION</span></span>
<span data-ttu-id="9224e-109">Gibt eine Liste aller Skalierungseinheiten Knoten an einer Position zurück.</span><span class="sxs-lookup"><span data-stu-id="9224e-109">Returns a list of all scale unit nodes in a location.</span></span>

## <span data-ttu-id="9224e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9224e-110">EXAMPLES</span></span>

### <span data-ttu-id="9224e-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9224e-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsScaleUnitNode
```

<span data-ttu-id="9224e-112">Rufen Sie alle Skalierungseinheiten Knoten an einer Position ab.</span><span class="sxs-lookup"><span data-stu-id="9224e-112">Get all scale unit nodes at a location.</span></span>

### <span data-ttu-id="9224e-113">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="9224e-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsScaleUnitNode -Name "HC1n25r2231"
```

<span data-ttu-id="9224e-114">Abrufen eines bestimmten Skalierungseinheiten Knotens an einem Speicherort, der einen Namen erhält.</span><span class="sxs-lookup"><span data-stu-id="9224e-114">Get a specific scale unit node at a location given a name.</span></span>

## <span data-ttu-id="9224e-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="9224e-115">PARAMETERS</span></span>

### <span data-ttu-id="9224e-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="9224e-116">-Filter</span></span>
<span data-ttu-id="9224e-117">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="9224e-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="9224e-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="9224e-118">-Location</span></span>
<span data-ttu-id="9224e-119">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="9224e-119">Location of the resource.</span></span>

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

### <span data-ttu-id="9224e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="9224e-120">-Name</span></span>
<span data-ttu-id="9224e-121">Name des Knotens der Skalierungseinheit</span><span class="sxs-lookup"><span data-stu-id="9224e-121">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="9224e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9224e-122">-ResourceGroupName</span></span>
<span data-ttu-id="9224e-123">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="9224e-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="9224e-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="9224e-124">-ResourceId</span></span>
<span data-ttu-id="9224e-125">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="9224e-125">The resource id.</span></span>

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

### <span data-ttu-id="9224e-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="9224e-126">-Skip</span></span>
<span data-ttu-id="9224e-127">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="9224e-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="9224e-128">-Top</span><span class="sxs-lookup"><span data-stu-id="9224e-128">-Top</span></span>
<span data-ttu-id="9224e-129">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="9224e-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="9224e-130">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="9224e-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="9224e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9224e-131">CommonParameters</span></span>
<span data-ttu-id="9224e-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9224e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9224e-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9224e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9224e-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9224e-134">INPUTS</span></span>

## <span data-ttu-id="9224e-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9224e-135">OUTPUTS</span></span>

### <span data-ttu-id="9224e-136">Microsoft. AzureStack. Management. Fabric. admin. Models. ScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="9224e-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.ScaleUnitNode</span></span>

## <span data-ttu-id="9224e-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="9224e-137">NOTES</span></span>

## <span data-ttu-id="9224e-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9224e-138">RELATED LINKS</span></span>

