---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc074d17ea73bf54f623ea3e8ec72567ef2bcffe
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827599"
---
# <span data-ttu-id="46d58-101">Get-AzsInfrastructureLocation</span><span class="sxs-lookup"><span data-stu-id="46d58-101">Get-AzsInfrastructureLocation</span></span>

## <span data-ttu-id="46d58-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="46d58-102">SYNOPSIS</span></span>
<span data-ttu-id="46d58-103">Gibt eine Liste aller Fabric-Speicherorte zurück.</span><span class="sxs-lookup"><span data-stu-id="46d58-103">Returns a list of all fabric locations.</span></span>

## <span data-ttu-id="46d58-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="46d58-104">SYNTAX</span></span>

### <span data-ttu-id="46d58-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="46d58-105">List (Default)</span></span>
```
Get-AzsInfrastructureLocation [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="46d58-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="46d58-106">Get</span></span>
```
Get-AzsInfrastructureLocation [-Location] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="46d58-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="46d58-107">ResourceId</span></span>
```
Get-AzsInfrastructureLocation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="46d58-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46d58-108">DESCRIPTION</span></span>
<span data-ttu-id="46d58-109">Gibt eine Liste aller Fabric-Speicherorte zurück.</span><span class="sxs-lookup"><span data-stu-id="46d58-109">Returns a list of all fabric locations.</span></span>

## <span data-ttu-id="46d58-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="46d58-110">EXAMPLES</span></span>

### <span data-ttu-id="46d58-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="46d58-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureLocation
```

<span data-ttu-id="46d58-112">Gibt eine Liste aller Fabric-Standorte zurück.</span><span class="sxs-lookup"><span data-stu-id="46d58-112">Return a list of all fabric locations.</span></span>

### <span data-ttu-id="46d58-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="46d58-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureLocation -Location "local"
```

<span data-ttu-id="46d58-114">Geben Sie einen Speicherort basierend auf dem Namen zurück.</span><span class="sxs-lookup"><span data-stu-id="46d58-114">Return a location based on the name.</span></span>

## <span data-ttu-id="46d58-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="46d58-115">PARAMETERS</span></span>

### <span data-ttu-id="46d58-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="46d58-116">-Location</span></span>
<span data-ttu-id="46d58-117">Fabric-Standort.</span><span class="sxs-lookup"><span data-stu-id="46d58-117">Fabric location.</span></span>

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

### <span data-ttu-id="46d58-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46d58-118">-ResourceGroupName</span></span>
<span data-ttu-id="46d58-119">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="46d58-119">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="46d58-120">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="46d58-120">-ResourceId</span></span>
<span data-ttu-id="46d58-121">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="46d58-121">The resource id.</span></span>

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

### <span data-ttu-id="46d58-122">-Filter</span><span class="sxs-lookup"><span data-stu-id="46d58-122">-Filter</span></span>
<span data-ttu-id="46d58-123">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="46d58-123">OData filter parameter.</span></span>

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

### <span data-ttu-id="46d58-124">-Skip</span><span class="sxs-lookup"><span data-stu-id="46d58-124">-Skip</span></span>
<span data-ttu-id="46d58-125">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="46d58-125">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="46d58-126">-Top</span><span class="sxs-lookup"><span data-stu-id="46d58-126">-Top</span></span>
<span data-ttu-id="46d58-127">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="46d58-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="46d58-128">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="46d58-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="46d58-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46d58-129">CommonParameters</span></span>
<span data-ttu-id="46d58-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46d58-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46d58-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46d58-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46d58-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="46d58-132">INPUTS</span></span>

## <span data-ttu-id="46d58-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="46d58-133">OUTPUTS</span></span>

### <span data-ttu-id="46d58-134">Microsoft. AzureStack. Management. Fabric. admin. Models. FabricLocation</span><span class="sxs-lookup"><span data-stu-id="46d58-134">Microsoft.AzureStack.Management.Fabric.Admin.Models.FabricLocation</span></span>

## <span data-ttu-id="46d58-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="46d58-135">NOTES</span></span>

## <span data-ttu-id="46d58-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="46d58-136">RELATED LINKS</span></span>
