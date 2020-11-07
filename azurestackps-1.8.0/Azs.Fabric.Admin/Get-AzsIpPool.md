---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d5999718cc3085eb69da482df27fa0cb4379ed40
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827583"
---
# <span data-ttu-id="87801-101">Get-AzsIpPool</span><span class="sxs-lookup"><span data-stu-id="87801-101">Get-AzsIpPool</span></span>

## <span data-ttu-id="87801-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="87801-102">SYNOPSIS</span></span>
<span data-ttu-id="87801-103">Gibt eine Liste aller IP-Pools an einer bestimmten Position zurück.</span><span class="sxs-lookup"><span data-stu-id="87801-103">Returns a list of all IP pools at a certain location.</span></span>

## <span data-ttu-id="87801-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="87801-104">SYNTAX</span></span>

### <span data-ttu-id="87801-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="87801-105">List (Default)</span></span>
```
Get-AzsIpPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="87801-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="87801-106">Get</span></span>
```
Get-AzsIpPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="87801-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="87801-107">ResourceId</span></span>
```
Get-AzsIpPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="87801-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="87801-108">DESCRIPTION</span></span>
<span data-ttu-id="87801-109">Gibt eine Liste aller IP-Pools an einer bestimmten Position zurück.</span><span class="sxs-lookup"><span data-stu-id="87801-109">Returns a list of all IP pools at a certain location.</span></span>

## <span data-ttu-id="87801-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="87801-110">EXAMPLES</span></span>

### <span data-ttu-id="87801-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="87801-111">EXAMPLE 1</span></span>
```
Get-AzsIpPool
```

<span data-ttu-id="87801-112">Abrufen aller IP-Pools für Infrastrukturen</span><span class="sxs-lookup"><span data-stu-id="87801-112">Get an all infrastructure ip pools.</span></span>

### <span data-ttu-id="87801-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="87801-113">EXAMPLE 2</span></span>
```
Get-AzsIpPool -Name "08786a0f-ad8c-43aa-a154-06083abfc1ac"
```

<span data-ttu-id="87801-114">Abrufen eines Infrastruktur-IP-Pools basierend auf dem Namen.</span><span class="sxs-lookup"><span data-stu-id="87801-114">Get an infrastructure ip pool based on name.</span></span>

## <span data-ttu-id="87801-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="87801-115">PARAMETERS</span></span>

### <span data-ttu-id="87801-116">-Name</span><span class="sxs-lookup"><span data-stu-id="87801-116">-Name</span></span>
<span data-ttu-id="87801-117">Name des IP-Pools.</span><span class="sxs-lookup"><span data-stu-id="87801-117">IP pool name.</span></span>

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

### <span data-ttu-id="87801-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="87801-118">-Location</span></span>
<span data-ttu-id="87801-119">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="87801-119">Location of the resource.</span></span>

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

### <span data-ttu-id="87801-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87801-120">-ResourceGroupName</span></span>
<span data-ttu-id="87801-121">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="87801-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="87801-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="87801-122">-ResourceId</span></span>
<span data-ttu-id="87801-123">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="87801-123">The resource id.</span></span>

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

### <span data-ttu-id="87801-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="87801-124">-Filter</span></span>
<span data-ttu-id="87801-125">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="87801-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="87801-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="87801-126">-Skip</span></span>
<span data-ttu-id="87801-127">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="87801-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="87801-128">-Top</span><span class="sxs-lookup"><span data-stu-id="87801-128">-Top</span></span>
<span data-ttu-id="87801-129">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="87801-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="87801-130">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="87801-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="87801-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87801-131">CommonParameters</span></span>
<span data-ttu-id="87801-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87801-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87801-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87801-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87801-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="87801-134">INPUTS</span></span>

## <span data-ttu-id="87801-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="87801-135">OUTPUTS</span></span>

### <span data-ttu-id="87801-136">Microsoft. AzureStack. Management. Fabric. admin. Models. IpPool</span><span class="sxs-lookup"><span data-stu-id="87801-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.IpPool</span></span>

## <span data-ttu-id="87801-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="87801-137">NOTES</span></span>

## <span data-ttu-id="87801-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="87801-138">RELATED LINKS</span></span>
