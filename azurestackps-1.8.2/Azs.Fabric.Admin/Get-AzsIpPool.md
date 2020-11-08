---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d5999718cc3085eb69da482df27fa0cb4379ed40
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94006873"
---
# <span data-ttu-id="2d8f3-101">Get-AzsIpPool</span><span class="sxs-lookup"><span data-stu-id="2d8f3-101">Get-AzsIpPool</span></span>

## <span data-ttu-id="2d8f3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2d8f3-102">SYNOPSIS</span></span>
<span data-ttu-id="2d8f3-103">Gibt eine Liste aller IP-Pools an einer bestimmten Position zurück.</span><span class="sxs-lookup"><span data-stu-id="2d8f3-103">Returns a list of all IP pools at a certain location.</span></span>

## <span data-ttu-id="2d8f3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d8f3-104">SYNTAX</span></span>

### <span data-ttu-id="2d8f3-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="2d8f3-105">List (Default)</span></span>
```
Get-AzsIpPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="2d8f3-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="2d8f3-106">Get</span></span>
```
Get-AzsIpPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="2d8f3-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d8f3-107">ResourceId</span></span>
```
Get-AzsIpPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="2d8f3-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2d8f3-108">DESCRIPTION</span></span>
<span data-ttu-id="2d8f3-109">Gibt eine Liste aller IP-Pools an einer bestimmten Position zurück.</span><span class="sxs-lookup"><span data-stu-id="2d8f3-109">Returns a list of all IP pools at a certain location.</span></span>

## <span data-ttu-id="2d8f3-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2d8f3-110">EXAMPLES</span></span>

### <span data-ttu-id="2d8f3-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2d8f3-111">EXAMPLE 1</span></span>
```
Get-AzsIpPool
```

<span data-ttu-id="2d8f3-112">Abrufen aller IP-Pools für Infrastrukturen</span><span class="sxs-lookup"><span data-stu-id="2d8f3-112">Get an all infrastructure ip pools.</span></span>

### <span data-ttu-id="2d8f3-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2d8f3-113">EXAMPLE 2</span></span>
```
Get-AzsIpPool -Name "08786a0f-ad8c-43aa-a154-06083abfc1ac"
```

<span data-ttu-id="2d8f3-114">Abrufen eines Infrastruktur-IP-Pools basierend auf dem Namen.</span><span class="sxs-lookup"><span data-stu-id="2d8f3-114">Get an infrastructure ip pool based on name.</span></span>

## <span data-ttu-id="2d8f3-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d8f3-115">PARAMETERS</span></span>

### <span data-ttu-id="2d8f3-116">-Name</span><span class="sxs-lookup"><span data-stu-id="2d8f3-116">-Name</span></span>
<span data-ttu-id="2d8f3-117">Name des IP-Pools.</span><span class="sxs-lookup"><span data-stu-id="2d8f3-117">IP pool name.</span></span>

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

### <span data-ttu-id="2d8f3-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="2d8f3-118">-Location</span></span>
<span data-ttu-id="2d8f3-119">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="2d8f3-119">Location of the resource.</span></span>

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

### <span data-ttu-id="2d8f3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d8f3-120">-ResourceGroupName</span></span>
<span data-ttu-id="2d8f3-121">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="2d8f3-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="2d8f3-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2d8f3-122">-ResourceId</span></span>
<span data-ttu-id="2d8f3-123">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="2d8f3-123">The resource id.</span></span>

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

### <span data-ttu-id="2d8f3-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="2d8f3-124">-Filter</span></span>
<span data-ttu-id="2d8f3-125">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="2d8f3-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="2d8f3-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="2d8f3-126">-Skip</span></span>
<span data-ttu-id="2d8f3-127">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="2d8f3-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="2d8f3-128">-Top</span><span class="sxs-lookup"><span data-stu-id="2d8f3-128">-Top</span></span>
<span data-ttu-id="2d8f3-129">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="2d8f3-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="2d8f3-130">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="2d8f3-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="2d8f3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d8f3-131">CommonParameters</span></span>
<span data-ttu-id="2d8f3-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d8f3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d8f3-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d8f3-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d8f3-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2d8f3-134">INPUTS</span></span>

## <span data-ttu-id="2d8f3-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2d8f3-135">OUTPUTS</span></span>

### <span data-ttu-id="2d8f3-136">Microsoft. AzureStack. Management. Fabric. admin. Models. IpPool</span><span class="sxs-lookup"><span data-stu-id="2d8f3-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.IpPool</span></span>

## <span data-ttu-id="2d8f3-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="2d8f3-137">NOTES</span></span>

## <span data-ttu-id="2d8f3-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2d8f3-138">RELATED LINKS</span></span>
