---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2528d9b4f9443d8857006b6fc1e94100b0b477ec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93827279"
---
# <span data-ttu-id="76078-101">Get-AzsIpPool</span><span class="sxs-lookup"><span data-stu-id="76078-101">Get-AzsIpPool</span></span>

## <span data-ttu-id="76078-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="76078-102">SYNOPSIS</span></span>
<span data-ttu-id="76078-103">Gibt eine Liste aller IP-Pools an einer bestimmten Position zurück.</span><span class="sxs-lookup"><span data-stu-id="76078-103">Returns a list of all IP pools at a certain location.</span></span>

## <span data-ttu-id="76078-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="76078-104">SYNTAX</span></span>

### <span data-ttu-id="76078-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="76078-105">List (Default)</span></span>
```
Get-AzsIpPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="76078-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="76078-106">Get</span></span>
```
Get-AzsIpPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="76078-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="76078-107">ResourceId</span></span>
```
Get-AzsIpPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="76078-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="76078-108">DESCRIPTION</span></span>
<span data-ttu-id="76078-109">Gibt eine Liste aller IP-Pools an einer bestimmten Position zurück.</span><span class="sxs-lookup"><span data-stu-id="76078-109">Returns a list of all IP pools at a certain location.</span></span>

## <span data-ttu-id="76078-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="76078-110">EXAMPLES</span></span>

### <span data-ttu-id="76078-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="76078-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsIpPool
```

<span data-ttu-id="76078-112">Abrufen aller IP-Pools für Infrastrukturen</span><span class="sxs-lookup"><span data-stu-id="76078-112">Get an all infrastructure ip pools.</span></span>

### <span data-ttu-id="76078-113">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="76078-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsIpPool -Name "08786a0f-ad8c-43aa-a154-06083abfc1ac"
```

<span data-ttu-id="76078-114">Abrufen eines Infrastruktur-IP-Pools basierend auf dem Namen.</span><span class="sxs-lookup"><span data-stu-id="76078-114">Get an infrastructure ip pool based on name.</span></span>

## <span data-ttu-id="76078-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="76078-115">PARAMETERS</span></span>

### <span data-ttu-id="76078-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="76078-116">-Filter</span></span>
<span data-ttu-id="76078-117">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="76078-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="76078-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="76078-118">-Location</span></span>
<span data-ttu-id="76078-119">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="76078-119">Location of the resource.</span></span>

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

### <span data-ttu-id="76078-120">-Name</span><span class="sxs-lookup"><span data-stu-id="76078-120">-Name</span></span>
<span data-ttu-id="76078-121">Name des IP-Pools.</span><span class="sxs-lookup"><span data-stu-id="76078-121">IP pool name.</span></span>

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

### <span data-ttu-id="76078-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76078-122">-ResourceGroupName</span></span>
<span data-ttu-id="76078-123">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="76078-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="76078-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="76078-124">-ResourceId</span></span>
<span data-ttu-id="76078-125">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="76078-125">The resource id.</span></span>

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

### <span data-ttu-id="76078-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="76078-126">-Skip</span></span>
<span data-ttu-id="76078-127">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="76078-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="76078-128">-Top</span><span class="sxs-lookup"><span data-stu-id="76078-128">-Top</span></span>
<span data-ttu-id="76078-129">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="76078-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="76078-130">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="76078-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="76078-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76078-131">CommonParameters</span></span>
<span data-ttu-id="76078-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76078-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76078-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76078-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76078-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="76078-134">INPUTS</span></span>

## <span data-ttu-id="76078-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="76078-135">OUTPUTS</span></span>

### <span data-ttu-id="76078-136">Microsoft. AzureStack. Management. Fabric. admin. Models. IpPool</span><span class="sxs-lookup"><span data-stu-id="76078-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.IpPool</span></span>

## <span data-ttu-id="76078-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="76078-137">NOTES</span></span>

## <span data-ttu-id="76078-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="76078-138">RELATED LINKS</span></span>

