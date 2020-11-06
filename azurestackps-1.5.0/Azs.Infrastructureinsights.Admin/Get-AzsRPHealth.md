---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7e42278eb4ed402d561399dbd1077f819ef3d2cd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475009"
---
# <span data-ttu-id="ecfd0-101">Get-AzsRPHealth</span><span class="sxs-lookup"><span data-stu-id="ecfd0-101">Get-AzsRPHealth</span></span>

## <span data-ttu-id="ecfd0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ecfd0-102">SYNOPSIS</span></span>
<span data-ttu-id="ecfd0-103">Gibt eine Liste der Integritätsstatus jedes Diensts zurück.</span><span class="sxs-lookup"><span data-stu-id="ecfd0-103">Returns a list of each service's health.</span></span>

## <span data-ttu-id="ecfd0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ecfd0-104">SYNTAX</span></span>

### <span data-ttu-id="ecfd0-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="ecfd0-105">List (Default)</span></span>
```
Get-AzsRPHealth [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="ecfd0-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="ecfd0-106">Get</span></span>
```
Get-AzsRPHealth [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="ecfd0-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ecfd0-107">ResourceId</span></span>
```
Get-AzsRPHealth -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="ecfd0-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ecfd0-108">DESCRIPTION</span></span>
<span data-ttu-id="ecfd0-109">Gibt eine Liste der Integritätsstatus jedes Diensts zurück.</span><span class="sxs-lookup"><span data-stu-id="ecfd0-109">Returns a list of each service's health.</span></span> <span data-ttu-id="ecfd0-110">Die AlertSummary-Eigenschaft enthält Details zur Warnung/Fehleranzahl.</span><span class="sxs-lookup"><span data-stu-id="ecfd0-110">The AlertSummary property includes details on warning/error counts.</span></span>

## <span data-ttu-id="ecfd0-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ecfd0-111">EXAMPLES</span></span>

### <span data-ttu-id="ecfd0-112">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ecfd0-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsRPHealth
```

<span data-ttu-id="ecfd0-113">Gibt eine Liste der Integritätsstatus jedes Diensts zurück.</span><span class="sxs-lookup"><span data-stu-id="ecfd0-113">Returns a list of each service's health.</span></span>

### <span data-ttu-id="ecfd0-114">--------------------------Beispiel 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="ecfd0-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsRPHealth -Name "e56bc7b8-c8b5-4e25-b00c-4f951effb22c"
```

<span data-ttu-id="ecfd0-115">Gibt den Status eines Diensts zurück.</span><span class="sxs-lookup"><span data-stu-id="ecfd0-115">Returns a service's health.</span></span>

## <span data-ttu-id="ecfd0-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="ecfd0-116">PARAMETERS</span></span>

### <span data-ttu-id="ecfd0-117">-Filter</span><span class="sxs-lookup"><span data-stu-id="ecfd0-117">-Filter</span></span>
<span data-ttu-id="ecfd0-118">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="ecfd0-118">OData filter parameter.</span></span>

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

### <span data-ttu-id="ecfd0-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="ecfd0-119">-Location</span></span>
<span data-ttu-id="ecfd0-120">Name der Region</span><span class="sxs-lookup"><span data-stu-id="ecfd0-120">Name of the region</span></span>

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

### <span data-ttu-id="ecfd0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="ecfd0-121">-Name</span></span>
<span data-ttu-id="ecfd0-122">Name des Dienststatus.</span><span class="sxs-lookup"><span data-stu-id="ecfd0-122">Service Health name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: ServiceHealth

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecfd0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecfd0-123">-ResourceGroupName</span></span>
<span data-ttu-id="ecfd0-124">Der Ressourcengruppenname, in dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="ecfd0-124">Resource group name which the resource resides.</span></span>

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

### <span data-ttu-id="ecfd0-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ecfd0-125">-ResourceId</span></span>
<span data-ttu-id="ecfd0-126">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="ecfd0-126">The resource id.</span></span>

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

### <span data-ttu-id="ecfd0-127">-Skip</span><span class="sxs-lookup"><span data-stu-id="ecfd0-127">-Skip</span></span>
<span data-ttu-id="ecfd0-128">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="ecfd0-128">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="ecfd0-129">-Top</span><span class="sxs-lookup"><span data-stu-id="ecfd0-129">-Top</span></span>
<span data-ttu-id="ecfd0-130">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="ecfd0-130">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="ecfd0-131">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="ecfd0-131">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="ecfd0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecfd0-132">CommonParameters</span></span>
<span data-ttu-id="ecfd0-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecfd0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecfd0-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecfd0-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecfd0-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ecfd0-135">INPUTS</span></span>

## <span data-ttu-id="ecfd0-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ecfd0-136">OUTPUTS</span></span>

### <span data-ttu-id="ecfd0-137">Microsoft. AzureStack. Management. InfrastructureInsights. admin. Models. ServiceHealth</span><span class="sxs-lookup"><span data-stu-id="ecfd0-137">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.ServiceHealth</span></span>

## <span data-ttu-id="ecfd0-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="ecfd0-138">NOTES</span></span>

## <span data-ttu-id="ecfd0-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ecfd0-139">RELATED LINKS</span></span>

