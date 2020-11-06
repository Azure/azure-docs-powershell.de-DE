---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 82ef5db457846f6fdf0dcd0a0a32b37cab96a557
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475633"
---
# <span data-ttu-id="276ce-101">Get-AzsLogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="276ce-101">Get-AzsLogicalSubnet</span></span>

## <span data-ttu-id="276ce-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="276ce-102">SYNOPSIS</span></span>
<span data-ttu-id="276ce-103">Gibt eine Liste aller logischen Subnetze zurück.</span><span class="sxs-lookup"><span data-stu-id="276ce-103">Returns a list of all logical subnets.</span></span>

## <span data-ttu-id="276ce-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="276ce-104">SYNTAX</span></span>

### <span data-ttu-id="276ce-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="276ce-105">List (Default)</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [-Filter <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="276ce-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="276ce-106">Get</span></span>
```
Get-AzsLogicalSubnet -Name <String> -LogicalNetwork <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="276ce-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="276ce-107">ResourceId</span></span>
```
Get-AzsLogicalSubnet -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="276ce-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="276ce-108">DESCRIPTION</span></span>
<span data-ttu-id="276ce-109">Gibt eine Liste aller logischen Subnetze zurück.</span><span class="sxs-lookup"><span data-stu-id="276ce-109">Returns a list of all logical subnets.</span></span>

## <span data-ttu-id="276ce-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="276ce-110">EXAMPLES</span></span>

### <span data-ttu-id="276ce-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="276ce-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001"
```

<span data-ttu-id="276ce-112">Abrufen einer Liste aller logischen Subnetze für ein bestimmtes logisches Netzwerk und einen bestimmten Speicherort.</span><span class="sxs-lookup"><span data-stu-id="276ce-112">Get a list of all logical subnets for a given logical network and location.</span></span>

### <span data-ttu-id="276ce-113">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="276ce-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsLogicalSubnet -LogicalNetwork "00000000-2222-1111-9999-000000000001" -Name "d8cfef2d-c0c8-4cdb-b0a8-fb1bdf3f2ad7"
```

<span data-ttu-id="276ce-114">Besorgen Sie sich ein bestimmtes logisches Subnetz für ein bestimmtes logisches Netzwerk und einen Speicherort basierend auf dem Namen.</span><span class="sxs-lookup"><span data-stu-id="276ce-114">Get a specific logical subnet for a given logical network and location based on name.</span></span>

## <span data-ttu-id="276ce-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="276ce-115">PARAMETERS</span></span>

### <span data-ttu-id="276ce-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="276ce-116">-Filter</span></span>
<span data-ttu-id="276ce-117">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="276ce-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="276ce-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="276ce-118">-Location</span></span>
<span data-ttu-id="276ce-119">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="276ce-119">Location of the resource.</span></span>

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

### <span data-ttu-id="276ce-120">-LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="276ce-120">-LogicalNetwork</span></span>
<span data-ttu-id="276ce-121">Der Name des logischen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="276ce-121">Name of the logical network.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="276ce-122">-Name</span><span class="sxs-lookup"><span data-stu-id="276ce-122">-Name</span></span>
<span data-ttu-id="276ce-123">Der Name des logischen Subnetzes.</span><span class="sxs-lookup"><span data-stu-id="276ce-123">Name of the logical subnet.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="276ce-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="276ce-124">-ResourceGroupName</span></span>
<span data-ttu-id="276ce-125">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="276ce-125">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="276ce-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="276ce-126">-ResourceId</span></span>
<span data-ttu-id="276ce-127">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="276ce-127">The resource id.</span></span>

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

### <span data-ttu-id="276ce-128">-Skip</span><span class="sxs-lookup"><span data-stu-id="276ce-128">-Skip</span></span>
<span data-ttu-id="276ce-129">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="276ce-129">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="276ce-130">-Top</span><span class="sxs-lookup"><span data-stu-id="276ce-130">-Top</span></span>
<span data-ttu-id="276ce-131">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="276ce-131">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="276ce-132">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="276ce-132">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="276ce-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="276ce-133">CommonParameters</span></span>
<span data-ttu-id="276ce-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="276ce-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="276ce-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="276ce-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="276ce-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="276ce-136">INPUTS</span></span>

## <span data-ttu-id="276ce-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="276ce-137">OUTPUTS</span></span>

### <span data-ttu-id="276ce-138">Microsoft. AzureStack. Management. Fabric. admin. Models. LogicalSubnet</span><span class="sxs-lookup"><span data-stu-id="276ce-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.LogicalSubnet</span></span>

## <span data-ttu-id="276ce-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="276ce-139">NOTES</span></span>

## <span data-ttu-id="276ce-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="276ce-140">RELATED LINKS</span></span>

