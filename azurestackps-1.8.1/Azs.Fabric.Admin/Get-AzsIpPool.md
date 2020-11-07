---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d5999718cc3085eb69da482df27fa0cb4379ed40
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93828263"
---
# <span data-ttu-id="036a2-101">Get-AzsIpPool</span><span class="sxs-lookup"><span data-stu-id="036a2-101">Get-AzsIpPool</span></span>

## <span data-ttu-id="036a2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="036a2-102">SYNOPSIS</span></span>
<span data-ttu-id="036a2-103">Gibt eine Liste aller IP-Pools an einer bestimmten Position zurück.</span><span class="sxs-lookup"><span data-stu-id="036a2-103">Returns a list of all IP pools at a certain location.</span></span>

## <span data-ttu-id="036a2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="036a2-104">SYNTAX</span></span>

### <span data-ttu-id="036a2-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="036a2-105">List (Default)</span></span>
```
Get-AzsIpPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="036a2-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="036a2-106">Get</span></span>
```
Get-AzsIpPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="036a2-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="036a2-107">ResourceId</span></span>
```
Get-AzsIpPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="036a2-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="036a2-108">DESCRIPTION</span></span>
<span data-ttu-id="036a2-109">Gibt eine Liste aller IP-Pools an einer bestimmten Position zurück.</span><span class="sxs-lookup"><span data-stu-id="036a2-109">Returns a list of all IP pools at a certain location.</span></span>

## <span data-ttu-id="036a2-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="036a2-110">EXAMPLES</span></span>

### <span data-ttu-id="036a2-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="036a2-111">EXAMPLE 1</span></span>
```
Get-AzsIpPool
```

<span data-ttu-id="036a2-112">Abrufen aller IP-Pools für Infrastrukturen</span><span class="sxs-lookup"><span data-stu-id="036a2-112">Get an all infrastructure ip pools.</span></span>

### <span data-ttu-id="036a2-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="036a2-113">EXAMPLE 2</span></span>
```
Get-AzsIpPool -Name "08786a0f-ad8c-43aa-a154-06083abfc1ac"
```

<span data-ttu-id="036a2-114">Abrufen eines Infrastruktur-IP-Pools basierend auf dem Namen.</span><span class="sxs-lookup"><span data-stu-id="036a2-114">Get an infrastructure ip pool based on name.</span></span>

## <span data-ttu-id="036a2-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="036a2-115">PARAMETERS</span></span>

### <span data-ttu-id="036a2-116">-Name</span><span class="sxs-lookup"><span data-stu-id="036a2-116">-Name</span></span>
<span data-ttu-id="036a2-117">Name des IP-Pools.</span><span class="sxs-lookup"><span data-stu-id="036a2-117">IP pool name.</span></span>

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

### <span data-ttu-id="036a2-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="036a2-118">-Location</span></span>
<span data-ttu-id="036a2-119">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="036a2-119">Location of the resource.</span></span>

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

### <span data-ttu-id="036a2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="036a2-120">-ResourceGroupName</span></span>
<span data-ttu-id="036a2-121">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="036a2-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="036a2-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="036a2-122">-ResourceId</span></span>
<span data-ttu-id="036a2-123">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="036a2-123">The resource id.</span></span>

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

### <span data-ttu-id="036a2-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="036a2-124">-Filter</span></span>
<span data-ttu-id="036a2-125">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="036a2-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="036a2-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="036a2-126">-Skip</span></span>
<span data-ttu-id="036a2-127">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="036a2-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="036a2-128">-Top</span><span class="sxs-lookup"><span data-stu-id="036a2-128">-Top</span></span>
<span data-ttu-id="036a2-129">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="036a2-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="036a2-130">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="036a2-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="036a2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="036a2-131">CommonParameters</span></span>
<span data-ttu-id="036a2-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="036a2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="036a2-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="036a2-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="036a2-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="036a2-134">INPUTS</span></span>

## <span data-ttu-id="036a2-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="036a2-135">OUTPUTS</span></span>

### <span data-ttu-id="036a2-136">Microsoft. AzureStack. Management. Fabric. admin. Models. IpPool</span><span class="sxs-lookup"><span data-stu-id="036a2-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.IpPool</span></span>

## <span data-ttu-id="036a2-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="036a2-137">NOTES</span></span>

## <span data-ttu-id="036a2-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="036a2-138">RELATED LINKS</span></span>
