---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c1ab041d888a43f498e694be9bc2e103422177f7
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93828196"
---
# <span data-ttu-id="c8934-101">Get-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="c8934-101">Get-AzsOfferDelegation</span></span>

## <span data-ttu-id="c8934-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c8934-102">SYNOPSIS</span></span>
<span data-ttu-id="c8934-103">Rufen Sie die Liste der Delegierten Angebote ab.</span><span class="sxs-lookup"><span data-stu-id="c8934-103">Get the list of delegated offers.</span></span>

## <span data-ttu-id="c8934-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8934-104">SYNTAX</span></span>

### <span data-ttu-id="c8934-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="c8934-105">List (Default)</span></span>
```
Get-AzsOfferDelegation -OfferName <String> -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="c8934-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="c8934-106">Get</span></span>
```
Get-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="c8934-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c8934-107">ResourceId</span></span>
```
Get-AzsOfferDelegation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="c8934-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c8934-108">DESCRIPTION</span></span>
<span data-ttu-id="c8934-109">Rufen Sie die Liste der Delegierten Angebote ab.</span><span class="sxs-lookup"><span data-stu-id="c8934-109">Get the list of delegated offers.</span></span>

## <span data-ttu-id="c8934-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c8934-110">EXAMPLES</span></span>

### <span data-ttu-id="c8934-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c8934-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1
```

<span data-ttu-id="c8934-112">Rufen Sie die Liste der Delegierten Angebote ab.</span><span class="sxs-lookup"><span data-stu-id="c8934-112">Get the list of delegated offers.</span></span>

## <span data-ttu-id="c8934-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8934-113">PARAMETERS</span></span>

### <span data-ttu-id="c8934-114">-Name</span><span class="sxs-lookup"><span data-stu-id="c8934-114">-Name</span></span>
<span data-ttu-id="c8934-115">Der Name einer Angebots Delegation.</span><span class="sxs-lookup"><span data-stu-id="c8934-115">Name of a offer delegation.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8934-116">-Angebotname</span><span class="sxs-lookup"><span data-stu-id="c8934-116">-OfferName</span></span>
<span data-ttu-id="c8934-117">Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="c8934-117">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8934-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8934-118">-ResourceGroupName</span></span>
<span data-ttu-id="c8934-119">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="c8934-119">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8934-120">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c8934-120">-ResourceId</span></span>
<span data-ttu-id="c8934-121">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="c8934-121">The resource id.</span></span>

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

### <span data-ttu-id="c8934-122">-Skip</span><span class="sxs-lookup"><span data-stu-id="c8934-122">-Skip</span></span>
<span data-ttu-id="c8934-123">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="c8934-123">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="c8934-124">-Top</span><span class="sxs-lookup"><span data-stu-id="c8934-124">-Top</span></span>
<span data-ttu-id="c8934-125">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="c8934-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="c8934-126">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="c8934-126">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="c8934-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8934-127">CommonParameters</span></span>
<span data-ttu-id="c8934-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8934-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8934-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8934-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8934-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c8934-130">INPUTS</span></span>

## <span data-ttu-id="c8934-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c8934-131">OUTPUTS</span></span>

### <span data-ttu-id="c8934-132">Microsoft. AzureStack. Management. Subscriptions. admin. Models. OfferDelegation</span><span class="sxs-lookup"><span data-stu-id="c8934-132">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="c8934-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="c8934-133">NOTES</span></span>

## <span data-ttu-id="c8934-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c8934-134">RELATED LINKS</span></span>

