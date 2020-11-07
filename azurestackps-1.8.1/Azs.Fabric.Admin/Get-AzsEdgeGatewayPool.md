---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a1f1be36f51aab748ec790c56aea7092f1d3d877
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93828292"
---
# <span data-ttu-id="93b99-101">Get-AzsEdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="93b99-101">Get-AzsEdgeGatewayPool</span></span>

## <span data-ttu-id="93b99-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="93b99-102">SYNOPSIS</span></span>
<span data-ttu-id="93b99-103">Gibt Gateway-Pool Objekte an einem Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="93b99-103">Returns gateway pool objects at a location.</span></span>

## <span data-ttu-id="93b99-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="93b99-104">SYNTAX</span></span>

### <span data-ttu-id="93b99-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="93b99-105">List (Default)</span></span>
```
Get-AzsEdgeGatewayPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="93b99-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="93b99-106">Get</span></span>
```
Get-AzsEdgeGatewayPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="93b99-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="93b99-107">ResourceId</span></span>
```
Get-AzsEdgeGatewayPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="93b99-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="93b99-108">DESCRIPTION</span></span>
<span data-ttu-id="93b99-109">Gibt Edge-Gateway-Pool Objekte an einem Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="93b99-109">Returns edge gateway pool objects at a location.</span></span>

## <span data-ttu-id="93b99-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="93b99-110">EXAMPLES</span></span>

### <span data-ttu-id="93b99-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="93b99-111">EXAMPLE 1</span></span>
```
Get-AzsEdgeGatewayPool
```

<span data-ttu-id="93b99-112">Abrufen einer Liste aller Edge-Gateway-Pools.</span><span class="sxs-lookup"><span data-stu-id="93b99-112">Get a list of all Edge Gateway pools.</span></span>

### <span data-ttu-id="93b99-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="93b99-113">EXAMPLE 2</span></span>
```
Get-AzsEdgeGatewayPool -Name "AzS-Gwy01"
```

<span data-ttu-id="93b99-114">Abrufen eines bestimmten Edge-Gateway-Pools.</span><span class="sxs-lookup"><span data-stu-id="93b99-114">Get a specific edge gateway pool.</span></span>

## <span data-ttu-id="93b99-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="93b99-115">PARAMETERS</span></span>

### <span data-ttu-id="93b99-116">-Name</span><span class="sxs-lookup"><span data-stu-id="93b99-116">-Name</span></span>
<span data-ttu-id="93b99-117">Name des Edge-Gateway-Pools.</span><span class="sxs-lookup"><span data-stu-id="93b99-117">Name of the edge gateway pool.</span></span>

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

### <span data-ttu-id="93b99-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="93b99-118">-Location</span></span>
<span data-ttu-id="93b99-119">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="93b99-119">Location of the resource.</span></span>

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

### <span data-ttu-id="93b99-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93b99-120">-ResourceGroupName</span></span>
<span data-ttu-id="93b99-121">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="93b99-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="93b99-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="93b99-122">-ResourceId</span></span>
<span data-ttu-id="93b99-123">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="93b99-123">The resource id.</span></span>

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

### <span data-ttu-id="93b99-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="93b99-124">-Filter</span></span>
<span data-ttu-id="93b99-125">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="93b99-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="93b99-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="93b99-126">-Skip</span></span>
<span data-ttu-id="93b99-127">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="93b99-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="93b99-128">-Top</span><span class="sxs-lookup"><span data-stu-id="93b99-128">-Top</span></span>
<span data-ttu-id="93b99-129">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="93b99-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="93b99-130">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="93b99-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="93b99-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93b99-131">CommonParameters</span></span>
<span data-ttu-id="93b99-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93b99-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93b99-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93b99-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93b99-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="93b99-134">INPUTS</span></span>

## <span data-ttu-id="93b99-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="93b99-135">OUTPUTS</span></span>

### <span data-ttu-id="93b99-136">Microsoft. AzureStack. Management. Fabric. admin. Models. EdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="93b99-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.EdgeGatewayPool</span></span>

## <span data-ttu-id="93b99-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="93b99-137">NOTES</span></span>

## <span data-ttu-id="93b99-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="93b99-138">RELATED LINKS</span></span>
