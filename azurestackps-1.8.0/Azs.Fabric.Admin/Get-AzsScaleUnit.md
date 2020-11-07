---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 475f8913731e8663cec6c6de4c89254c47d7af5e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827571"
---
# <span data-ttu-id="439ad-101">Get-AzsScaleUnit</span><span class="sxs-lookup"><span data-stu-id="439ad-101">Get-AzsScaleUnit</span></span>

## <span data-ttu-id="439ad-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="439ad-102">SYNOPSIS</span></span>
<span data-ttu-id="439ad-103">Gibt eine Liste aller Skaleneinheiten an einer Position zurück.</span><span class="sxs-lookup"><span data-stu-id="439ad-103">Returns a list of all scale units at a location.</span></span>

## <span data-ttu-id="439ad-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="439ad-104">SYNTAX</span></span>

### <span data-ttu-id="439ad-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="439ad-105">List (Default)</span></span>
```
Get-AzsScaleUnit [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="439ad-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="439ad-106">Get</span></span>
```
Get-AzsScaleUnit [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="439ad-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="439ad-107">ResourceId</span></span>
```
Get-AzsScaleUnit -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="439ad-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="439ad-108">DESCRIPTION</span></span>
<span data-ttu-id="439ad-109">Gibt eine Liste aller Skaleneinheiten an einer Position zurück.</span><span class="sxs-lookup"><span data-stu-id="439ad-109">Returns a list of all scale units at a location.</span></span>

## <span data-ttu-id="439ad-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="439ad-110">EXAMPLES</span></span>

### <span data-ttu-id="439ad-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="439ad-111">EXAMPLE 1</span></span>
```
Get-AzsScaleUnit
```

<span data-ttu-id="439ad-112">Geben Sie eine Liste mit Informationen zu Skaleneinheiten zurück.</span><span class="sxs-lookup"><span data-stu-id="439ad-112">Return a list of information about scale units.</span></span>

### <span data-ttu-id="439ad-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="439ad-113">EXAMPLE 2</span></span>
```
Get-AzsScaleUnit -Name "S-Cluster"
```

<span data-ttu-id="439ad-114">Gibt Informationen zu einer bestimmten Skalierungseinheit zurück.</span><span class="sxs-lookup"><span data-stu-id="439ad-114">Return information about a specific scale unit.</span></span>

## <span data-ttu-id="439ad-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="439ad-115">PARAMETERS</span></span>

### <span data-ttu-id="439ad-116">-Name</span><span class="sxs-lookup"><span data-stu-id="439ad-116">-Name</span></span>
<span data-ttu-id="439ad-117">Name der Skalierungseinheiten</span><span class="sxs-lookup"><span data-stu-id="439ad-117">Name of the scale units.</span></span>

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

### <span data-ttu-id="439ad-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="439ad-118">-Location</span></span>
<span data-ttu-id="439ad-119">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="439ad-119">Location of the resource.</span></span>

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

### <span data-ttu-id="439ad-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="439ad-120">-ResourceGroupName</span></span>
<span data-ttu-id="439ad-121">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="439ad-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="439ad-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="439ad-122">-ResourceId</span></span>
<span data-ttu-id="439ad-123">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="439ad-123">The resource id.</span></span>

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

### <span data-ttu-id="439ad-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="439ad-124">-Filter</span></span>
<span data-ttu-id="439ad-125">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="439ad-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="439ad-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="439ad-126">-Skip</span></span>
<span data-ttu-id="439ad-127">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="439ad-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="439ad-128">-Top</span><span class="sxs-lookup"><span data-stu-id="439ad-128">-Top</span></span>
<span data-ttu-id="439ad-129">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="439ad-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="439ad-130">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="439ad-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="439ad-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="439ad-131">CommonParameters</span></span>
<span data-ttu-id="439ad-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="439ad-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="439ad-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="439ad-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="439ad-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="439ad-134">INPUTS</span></span>

## <span data-ttu-id="439ad-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="439ad-135">OUTPUTS</span></span>

### <span data-ttu-id="439ad-136">Microsoft. AzureStack. Management. Fabric. admin. Models. ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="439ad-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.ScaleUnit</span></span>

## <span data-ttu-id="439ad-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="439ad-137">NOTES</span></span>

## <span data-ttu-id="439ad-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="439ad-138">RELATED LINKS</span></span>
