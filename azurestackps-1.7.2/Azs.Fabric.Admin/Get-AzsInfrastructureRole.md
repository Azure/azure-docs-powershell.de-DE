---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: dac95eced72f70d3471019136d302fcdfe95f86b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93827284"
---
# <span data-ttu-id="f3ed2-101">Get-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="f3ed2-101">Get-AzsInfrastructureRole</span></span>

## <span data-ttu-id="f3ed2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f3ed2-102">SYNOPSIS</span></span>
<span data-ttu-id="f3ed2-103">Gibt eine Liste aller Infrastrukturrollen an einem Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="f3ed2-103">Returns a list of all infrastructure roles at a location.</span></span>

## <span data-ttu-id="f3ed2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3ed2-104">SYNTAX</span></span>

### <span data-ttu-id="f3ed2-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="f3ed2-105">List (Default)</span></span>
```
Get-AzsInfrastructureRole [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="f3ed2-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="f3ed2-106">Get</span></span>
```
Get-AzsInfrastructureRole [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3ed2-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3ed2-107">ResourceId</span></span>
```
Get-AzsInfrastructureRole -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="f3ed2-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3ed2-108">DESCRIPTION</span></span>
<span data-ttu-id="f3ed2-109">Gibt eine Liste aller Infrastrukturrollen an einem Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="f3ed2-109">Returns a list of all infrastructure roles at a location.</span></span>

## <span data-ttu-id="f3ed2-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f3ed2-110">EXAMPLES</span></span>

### <span data-ttu-id="f3ed2-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f3ed2-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsInfrastructureRole
```

<span data-ttu-id="f3ed2-112">Abrufen einer Liste aller Infrastrukturrollen</span><span class="sxs-lookup"><span data-stu-id="f3ed2-112">Get a list of all infrastructure roles.</span></span>

### <span data-ttu-id="f3ed2-113">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="f3ed2-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsInfrastructureRole -Name "Active Directory Federation Services"
```

<span data-ttu-id="f3ed2-114">Abrufen einer Infrastruktur Rolle basierend auf dem Namen.</span><span class="sxs-lookup"><span data-stu-id="f3ed2-114">Get an infrastructure role based on the name.</span></span>

## <span data-ttu-id="f3ed2-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3ed2-115">PARAMETERS</span></span>

### <span data-ttu-id="f3ed2-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="f3ed2-116">-Filter</span></span>
<span data-ttu-id="f3ed2-117">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="f3ed2-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="f3ed2-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="f3ed2-118">-Location</span></span>
<span data-ttu-id="f3ed2-119">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="f3ed2-119">Location of the resource.</span></span>

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

### <span data-ttu-id="f3ed2-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f3ed2-120">-Name</span></span>
<span data-ttu-id="f3ed2-121">Name der Infrastruktur Rolle</span><span class="sxs-lookup"><span data-stu-id="f3ed2-121">Infrastructure role name.</span></span>

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

### <span data-ttu-id="f3ed2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3ed2-122">-ResourceGroupName</span></span>
<span data-ttu-id="f3ed2-123">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="f3ed2-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="f3ed2-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f3ed2-124">-ResourceId</span></span>
<span data-ttu-id="f3ed2-125">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="f3ed2-125">The resource id.</span></span>

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

### <span data-ttu-id="f3ed2-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="f3ed2-126">-Skip</span></span>
<span data-ttu-id="f3ed2-127">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="f3ed2-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="f3ed2-128">-Top</span><span class="sxs-lookup"><span data-stu-id="f3ed2-128">-Top</span></span>
<span data-ttu-id="f3ed2-129">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="f3ed2-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="f3ed2-130">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="f3ed2-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="f3ed2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3ed2-131">CommonParameters</span></span>
<span data-ttu-id="f3ed2-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3ed2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3ed2-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3ed2-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3ed2-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f3ed2-134">INPUTS</span></span>

## <span data-ttu-id="f3ed2-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f3ed2-135">OUTPUTS</span></span>

### <span data-ttu-id="f3ed2-136">Microsoft. AzureStack. Management. Fabric. admin. Models. InfraRole</span><span class="sxs-lookup"><span data-stu-id="f3ed2-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.InfraRole</span></span>

## <span data-ttu-id="f3ed2-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="f3ed2-137">NOTES</span></span>

## <span data-ttu-id="f3ed2-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f3ed2-138">RELATED LINKS</span></span>

