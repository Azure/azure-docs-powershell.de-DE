---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc074d17ea73bf54f623ea3e8ec72567ef2bcffe
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93828287"
---
# <span data-ttu-id="660c5-101">Get-AzsInfrastructureLocation</span><span class="sxs-lookup"><span data-stu-id="660c5-101">Get-AzsInfrastructureLocation</span></span>

## <span data-ttu-id="660c5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="660c5-102">SYNOPSIS</span></span>
<span data-ttu-id="660c5-103">Gibt eine Liste aller Fabric-Speicherorte zurück.</span><span class="sxs-lookup"><span data-stu-id="660c5-103">Returns a list of all fabric locations.</span></span>

## <span data-ttu-id="660c5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="660c5-104">SYNTAX</span></span>

### <span data-ttu-id="660c5-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="660c5-105">List (Default)</span></span>
```
Get-AzsInfrastructureLocation [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="660c5-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="660c5-106">Get</span></span>
```
Get-AzsInfrastructureLocation [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="660c5-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="660c5-107">ResourceId</span></span>
```
Get-AzsInfrastructureLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="660c5-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="660c5-108">DESCRIPTION</span></span>
<span data-ttu-id="660c5-109">Gibt eine Liste aller Fabric-Speicherorte zurück.</span><span class="sxs-lookup"><span data-stu-id="660c5-109">Returns a list of all fabric locations.</span></span>

## <span data-ttu-id="660c5-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="660c5-110">EXAMPLES</span></span>

### <span data-ttu-id="660c5-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="660c5-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureLocation
```

<span data-ttu-id="660c5-112">Gibt eine Liste aller Fabric-Standorte zurück.</span><span class="sxs-lookup"><span data-stu-id="660c5-112">Return a list of all fabric locations.</span></span>

### <span data-ttu-id="660c5-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="660c5-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureLocation -Location "local"
```

<span data-ttu-id="660c5-114">Geben Sie einen Speicherort basierend auf dem Namen zurück.</span><span class="sxs-lookup"><span data-stu-id="660c5-114">Return a location based on the name.</span></span>

## <span data-ttu-id="660c5-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="660c5-115">PARAMETERS</span></span>

### <span data-ttu-id="660c5-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="660c5-116">-Location</span></span>
<span data-ttu-id="660c5-117">Fabric-Standort.</span><span class="sxs-lookup"><span data-stu-id="660c5-117">Fabric location.</span></span>

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

### <span data-ttu-id="660c5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="660c5-118">-ResourceGroupName</span></span>
<span data-ttu-id="660c5-119">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="660c5-119">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="660c5-120">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="660c5-120">-ResourceId</span></span>
<span data-ttu-id="660c5-121">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="660c5-121">The resource id.</span></span>

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

### <span data-ttu-id="660c5-122">-Filter</span><span class="sxs-lookup"><span data-stu-id="660c5-122">-Filter</span></span>
<span data-ttu-id="660c5-123">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="660c5-123">OData filter parameter.</span></span>

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

### <span data-ttu-id="660c5-124">-Skip</span><span class="sxs-lookup"><span data-stu-id="660c5-124">-Skip</span></span>
<span data-ttu-id="660c5-125">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="660c5-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="660c5-126">-Top</span><span class="sxs-lookup"><span data-stu-id="660c5-126">-Top</span></span>
<span data-ttu-id="660c5-127">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="660c5-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="660c5-128">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="660c5-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="660c5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="660c5-129">CommonParameters</span></span>
<span data-ttu-id="660c5-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="660c5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="660c5-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="660c5-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="660c5-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="660c5-132">INPUTS</span></span>

## <span data-ttu-id="660c5-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="660c5-133">OUTPUTS</span></span>

### <span data-ttu-id="660c5-134">Microsoft. AzureStack. Management. Fabric. admin. Models. FabricLocation</span><span class="sxs-lookup"><span data-stu-id="660c5-134">Microsoft.AzureStack.Management.Fabric.Admin.Models.FabricLocation</span></span>

## <span data-ttu-id="660c5-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="660c5-135">NOTES</span></span>

## <span data-ttu-id="660c5-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="660c5-136">RELATED LINKS</span></span>
