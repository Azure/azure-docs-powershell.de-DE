---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a81fcf688e1c269aabd64250e9b0694730edc8f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93474601"
---
# <span data-ttu-id="4dbbc-101">Get-AzsEdgeGateway</span><span class="sxs-lookup"><span data-stu-id="4dbbc-101">Get-AzsEdgeGateway</span></span>

## <span data-ttu-id="4dbbc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4dbbc-102">SYNOPSIS</span></span>
<span data-ttu-id="4dbbc-103">Gibt die Liste aller Edge-Gateways an einer bestimmten Position zurück.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-103">Returns the list of all edge gateways at a certain location.</span></span>

## <span data-ttu-id="4dbbc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4dbbc-104">SYNTAX</span></span>

### <span data-ttu-id="4dbbc-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="4dbbc-105">List (Default)</span></span>
```
Get-AzsEdgeGateway [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="4dbbc-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="4dbbc-106">Get</span></span>
```
Get-AzsEdgeGateway [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="4dbbc-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4dbbc-107">ResourceId</span></span>
```
Get-AzsEdgeGateway -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="4dbbc-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4dbbc-108">DESCRIPTION</span></span>
<span data-ttu-id="4dbbc-109">Gibt die Liste aller Edge-Gateways an einer bestimmten Position zurück.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-109">Returns the list of all edge gateways at a certain location.</span></span>

## <span data-ttu-id="4dbbc-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4dbbc-110">EXAMPLES</span></span>

### <span data-ttu-id="4dbbc-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4dbbc-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsEdgeGateway
```

<span data-ttu-id="4dbbc-112">Abrufen einer Liste aller Edge-Gateways</span><span class="sxs-lookup"><span data-stu-id="4dbbc-112">Get a list of all edge gateways.</span></span>

### <span data-ttu-id="4dbbc-113">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="4dbbc-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsEdgeGateway -Name "AzS-Gwy01"
```

<span data-ttu-id="4dbbc-114">Besorgen Sie sich ein bestimmtes Edge-Gateway.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-114">Get a specific edge gateway.</span></span>

## <span data-ttu-id="4dbbc-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="4dbbc-115">PARAMETERS</span></span>

### <span data-ttu-id="4dbbc-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="4dbbc-116">-Filter</span></span>
<span data-ttu-id="4dbbc-117">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="4dbbc-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="4dbbc-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="4dbbc-118">-Location</span></span>
<span data-ttu-id="4dbbc-119">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-119">Location of the resource.</span></span>

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

### <span data-ttu-id="4dbbc-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4dbbc-120">-Name</span></span>
<span data-ttu-id="4dbbc-121">Der Name des Edge-Gateways.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-121">Name of the edge gateway.</span></span>

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

### <span data-ttu-id="4dbbc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dbbc-122">-ResourceGroupName</span></span>
<span data-ttu-id="4dbbc-123">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="4dbbc-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4dbbc-124">-ResourceId</span></span>
<span data-ttu-id="4dbbc-125">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-125">The resource id.</span></span>

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

### <span data-ttu-id="4dbbc-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="4dbbc-126">-Skip</span></span>
<span data-ttu-id="4dbbc-127">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="4dbbc-128">-Top</span><span class="sxs-lookup"><span data-stu-id="4dbbc-128">-Top</span></span>
<span data-ttu-id="4dbbc-129">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="4dbbc-130">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="4dbbc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dbbc-131">CommonParameters</span></span>
<span data-ttu-id="4dbbc-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dbbc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dbbc-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dbbc-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dbbc-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4dbbc-134">INPUTS</span></span>

## <span data-ttu-id="4dbbc-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4dbbc-135">OUTPUTS</span></span>

### <span data-ttu-id="4dbbc-136">Microsoft. AzureStack. Management. Fabric. admin. Models. EdgeGateway</span><span class="sxs-lookup"><span data-stu-id="4dbbc-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.EdgeGateway</span></span>

## <span data-ttu-id="4dbbc-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="4dbbc-137">NOTES</span></span>

## <span data-ttu-id="4dbbc-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4dbbc-138">RELATED LINKS</span></span>

