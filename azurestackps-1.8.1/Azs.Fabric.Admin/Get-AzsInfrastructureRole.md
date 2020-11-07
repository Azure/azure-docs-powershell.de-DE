---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4a20f0fbc5b059e878f0062569ffba2c16794204
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93828288"
---
# <span data-ttu-id="8ac16-101">Get-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="8ac16-101">Get-AzsInfrastructureRole</span></span>

## <span data-ttu-id="8ac16-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8ac16-102">SYNOPSIS</span></span>
<span data-ttu-id="8ac16-103">Gibt eine Liste aller Infrastrukturrollen an einem Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="8ac16-103">Returns a list of all infrastructure roles at a location.</span></span>

## <span data-ttu-id="8ac16-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ac16-104">SYNTAX</span></span>

### <span data-ttu-id="8ac16-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="8ac16-105">List (Default)</span></span>
```
Get-AzsInfrastructureRole [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="8ac16-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="8ac16-106">Get</span></span>
```
Get-AzsInfrastructureRole [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="8ac16-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ac16-107">ResourceId</span></span>
```
Get-AzsInfrastructureRole -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="8ac16-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8ac16-108">DESCRIPTION</span></span>
<span data-ttu-id="8ac16-109">Gibt eine Liste aller Infrastrukturrollen an einem Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="8ac16-109">Returns a list of all infrastructure roles at a location.</span></span>

## <span data-ttu-id="8ac16-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8ac16-110">EXAMPLES</span></span>

### <span data-ttu-id="8ac16-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8ac16-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureRole
```

<span data-ttu-id="8ac16-112">Abrufen einer Liste aller Infrastrukturrollen</span><span class="sxs-lookup"><span data-stu-id="8ac16-112">Get a list of all infrastructure roles.</span></span>

### <span data-ttu-id="8ac16-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8ac16-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureRole -Name "Active Directory Federation Services"
```

<span data-ttu-id="8ac16-114">Abrufen einer Infrastruktur Rolle basierend auf dem Namen.</span><span class="sxs-lookup"><span data-stu-id="8ac16-114">Get an infrastructure role based on the name.</span></span>

## <span data-ttu-id="8ac16-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ac16-115">PARAMETERS</span></span>

### <span data-ttu-id="8ac16-116">-Name</span><span class="sxs-lookup"><span data-stu-id="8ac16-116">-Name</span></span>
<span data-ttu-id="8ac16-117">Name der Infrastruktur Rolle</span><span class="sxs-lookup"><span data-stu-id="8ac16-117">Infrastructure role name.</span></span>

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

### <span data-ttu-id="8ac16-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="8ac16-118">-Location</span></span>
<span data-ttu-id="8ac16-119">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="8ac16-119">Location of the resource.</span></span>

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

### <span data-ttu-id="8ac16-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ac16-120">-ResourceGroupName</span></span>
<span data-ttu-id="8ac16-121">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="8ac16-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="8ac16-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="8ac16-122">-ResourceId</span></span>
<span data-ttu-id="8ac16-123">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="8ac16-123">The resource id.</span></span>

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

### <span data-ttu-id="8ac16-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="8ac16-124">-Filter</span></span>
<span data-ttu-id="8ac16-125">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="8ac16-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="8ac16-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="8ac16-126">-Skip</span></span>
<span data-ttu-id="8ac16-127">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="8ac16-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="8ac16-128">-Top</span><span class="sxs-lookup"><span data-stu-id="8ac16-128">-Top</span></span>
<span data-ttu-id="8ac16-129">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="8ac16-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="8ac16-130">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="8ac16-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="8ac16-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ac16-131">CommonParameters</span></span>
<span data-ttu-id="8ac16-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ac16-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ac16-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ac16-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ac16-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8ac16-134">INPUTS</span></span>

## <span data-ttu-id="8ac16-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8ac16-135">OUTPUTS</span></span>

### <span data-ttu-id="8ac16-136">Microsoft. AzureStack. Management. Fabric. admin. Models. InfraRole</span><span class="sxs-lookup"><span data-stu-id="8ac16-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.InfraRole</span></span>

## <span data-ttu-id="8ac16-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="8ac16-137">NOTES</span></span>

## <span data-ttu-id="8ac16-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8ac16-138">RELATED LINKS</span></span>
