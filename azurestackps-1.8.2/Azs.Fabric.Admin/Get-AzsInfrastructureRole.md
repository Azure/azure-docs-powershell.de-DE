---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4a20f0fbc5b059e878f0062569ffba2c16794204
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94006848"
---
# <span data-ttu-id="2608f-101">Get-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="2608f-101">Get-AzsInfrastructureRole</span></span>

## <span data-ttu-id="2608f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2608f-102">SYNOPSIS</span></span>
<span data-ttu-id="2608f-103">Gibt eine Liste aller Infrastrukturrollen an einem Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="2608f-103">Returns a list of all infrastructure roles at a location.</span></span>

## <span data-ttu-id="2608f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2608f-104">SYNTAX</span></span>

### <span data-ttu-id="2608f-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="2608f-105">List (Default)</span></span>
```
Get-AzsInfrastructureRole [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="2608f-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="2608f-106">Get</span></span>
```
Get-AzsInfrastructureRole [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="2608f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2608f-107">ResourceId</span></span>
```
Get-AzsInfrastructureRole -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="2608f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2608f-108">DESCRIPTION</span></span>
<span data-ttu-id="2608f-109">Gibt eine Liste aller Infrastrukturrollen an einem Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="2608f-109">Returns a list of all infrastructure roles at a location.</span></span>

## <span data-ttu-id="2608f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2608f-110">EXAMPLES</span></span>

### <span data-ttu-id="2608f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2608f-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureRole
```

<span data-ttu-id="2608f-112">Abrufen einer Liste aller Infrastrukturrollen</span><span class="sxs-lookup"><span data-stu-id="2608f-112">Get a list of all infrastructure roles.</span></span>

### <span data-ttu-id="2608f-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2608f-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureRole -Name "Active Directory Federation Services"
```

<span data-ttu-id="2608f-114">Abrufen einer Infrastruktur Rolle basierend auf dem Namen.</span><span class="sxs-lookup"><span data-stu-id="2608f-114">Get an infrastructure role based on the name.</span></span>

## <span data-ttu-id="2608f-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="2608f-115">PARAMETERS</span></span>

### <span data-ttu-id="2608f-116">-Name</span><span class="sxs-lookup"><span data-stu-id="2608f-116">-Name</span></span>
<span data-ttu-id="2608f-117">Name der Infrastruktur Rolle</span><span class="sxs-lookup"><span data-stu-id="2608f-117">Infrastructure role name.</span></span>

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

### <span data-ttu-id="2608f-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="2608f-118">-Location</span></span>
<span data-ttu-id="2608f-119">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="2608f-119">Location of the resource.</span></span>

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

### <span data-ttu-id="2608f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2608f-120">-ResourceGroupName</span></span>
<span data-ttu-id="2608f-121">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="2608f-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="2608f-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2608f-122">-ResourceId</span></span>
<span data-ttu-id="2608f-123">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="2608f-123">The resource id.</span></span>

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

### <span data-ttu-id="2608f-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="2608f-124">-Filter</span></span>
<span data-ttu-id="2608f-125">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="2608f-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="2608f-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="2608f-126">-Skip</span></span>
<span data-ttu-id="2608f-127">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="2608f-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="2608f-128">-Top</span><span class="sxs-lookup"><span data-stu-id="2608f-128">-Top</span></span>
<span data-ttu-id="2608f-129">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="2608f-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="2608f-130">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="2608f-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="2608f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2608f-131">CommonParameters</span></span>
<span data-ttu-id="2608f-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2608f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2608f-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2608f-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2608f-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2608f-134">INPUTS</span></span>

## <span data-ttu-id="2608f-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2608f-135">OUTPUTS</span></span>

### <span data-ttu-id="2608f-136">Microsoft. AzureStack. Management. Fabric. admin. Models. InfraRole</span><span class="sxs-lookup"><span data-stu-id="2608f-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.InfraRole</span></span>

## <span data-ttu-id="2608f-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="2608f-137">NOTES</span></span>

## <span data-ttu-id="2608f-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2608f-138">RELATED LINKS</span></span>
