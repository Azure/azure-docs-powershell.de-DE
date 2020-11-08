---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 821495581589eff356cd0d88fc98311b5f566d61
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94006842"
---
# <span data-ttu-id="44fa9-101">Get-AzsSlbMuxInstance</span><span class="sxs-lookup"><span data-stu-id="44fa9-101">Get-AzsSlbMuxInstance</span></span>

## <span data-ttu-id="44fa9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="44fa9-102">SYNOPSIS</span></span>
<span data-ttu-id="44fa9-103">Gibt eine Liste aller Instanzen des Software-Lastenausgleichs an einem Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="44fa9-103">Returns a list of all software load balancer instances at a location.</span></span>

## <span data-ttu-id="44fa9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="44fa9-104">SYNTAX</span></span>

### <span data-ttu-id="44fa9-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="44fa9-105">List (Default)</span></span>
```
Get-AzsSlbMuxInstance [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="44fa9-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="44fa9-106">Get</span></span>
```
Get-AzsSlbMuxInstance [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="44fa9-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="44fa9-107">ResourceId</span></span>
```
Get-AzsSlbMuxInstance -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="44fa9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="44fa9-108">DESCRIPTION</span></span>
<span data-ttu-id="44fa9-109">Gibt eine Liste aller Instanzen des Software-Lastenausgleichs an einem Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="44fa9-109">Returns a list of all software load balancer instances at a location.</span></span>

## <span data-ttu-id="44fa9-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="44fa9-110">EXAMPLES</span></span>

### <span data-ttu-id="44fa9-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="44fa9-111">EXAMPLE 1</span></span>
```
Get-AzsSlbMuxInstance
```

<span data-ttu-id="44fa9-112">Laden Sie die gesamte Software Load Balancer-Multiplexer-Instanz an einem Speicherort herunter.</span><span class="sxs-lookup"><span data-stu-id="44fa9-112">Get all software load balancer multiplexer instance at a location.</span></span>

### <span data-ttu-id="44fa9-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="44fa9-113">EXAMPLE 2</span></span>
```
Get-AzsSlbMuxInstance -Name "AzS-SLB01"
```

<span data-ttu-id="44fa9-114">Besorgen Sie sich eine bestimmte Multiplexer-Instanz des Software-Lastenausgleichs an einem Speicherort, der einen Namen erhält.</span><span class="sxs-lookup"><span data-stu-id="44fa9-114">Get a specific software load balancer multiplexer instance at a location given a name.</span></span>

## <span data-ttu-id="44fa9-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="44fa9-115">PARAMETERS</span></span>

### <span data-ttu-id="44fa9-116">-Name</span><span class="sxs-lookup"><span data-stu-id="44fa9-116">-Name</span></span>
<span data-ttu-id="44fa9-117">Der Name einer SLB-MUX-Instanz.</span><span class="sxs-lookup"><span data-stu-id="44fa9-117">Name of a SLB MUX instance.</span></span>

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

### <span data-ttu-id="44fa9-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="44fa9-118">-Location</span></span>
<span data-ttu-id="44fa9-119">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="44fa9-119">Location of the resource.</span></span>

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

### <span data-ttu-id="44fa9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44fa9-120">-ResourceGroupName</span></span>
<span data-ttu-id="44fa9-121">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="44fa9-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="44fa9-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="44fa9-122">-ResourceId</span></span>
<span data-ttu-id="44fa9-123">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="44fa9-123">The resource id.</span></span>

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

### <span data-ttu-id="44fa9-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="44fa9-124">-Filter</span></span>
<span data-ttu-id="44fa9-125">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="44fa9-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="44fa9-126">-Skip</span><span class="sxs-lookup"><span data-stu-id="44fa9-126">-Skip</span></span>
<span data-ttu-id="44fa9-127">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="44fa9-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="44fa9-128">-Top</span><span class="sxs-lookup"><span data-stu-id="44fa9-128">-Top</span></span>
<span data-ttu-id="44fa9-129">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="44fa9-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="44fa9-130">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="44fa9-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="44fa9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44fa9-131">CommonParameters</span></span>
<span data-ttu-id="44fa9-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44fa9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44fa9-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44fa9-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44fa9-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="44fa9-134">INPUTS</span></span>

## <span data-ttu-id="44fa9-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="44fa9-135">OUTPUTS</span></span>

### <span data-ttu-id="44fa9-136">Microsoft. AzureStack. Management. Fabric. admin. Models. SlbMuxInstance</span><span class="sxs-lookup"><span data-stu-id="44fa9-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.SlbMuxInstance</span></span>

## <span data-ttu-id="44fa9-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="44fa9-137">NOTES</span></span>

## <span data-ttu-id="44fa9-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="44fa9-138">RELATED LINKS</span></span>
