---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6c58e8dedf4f55a9e1fb6451bf7f774b766b6d71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475410"
---
# <span data-ttu-id="4338d-101">Get-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="4338d-101">Get-AzsOfferDelegation</span></span>

## <span data-ttu-id="4338d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4338d-102">SYNOPSIS</span></span>
<span data-ttu-id="4338d-103">Rufen Sie die Liste der Delegierten Angebote ab.</span><span class="sxs-lookup"><span data-stu-id="4338d-103">Get the list of delegated offers.</span></span>

## <span data-ttu-id="4338d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4338d-104">SYNTAX</span></span>

### <span data-ttu-id="4338d-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="4338d-105">List (Default)</span></span>
```
Get-AzsOfferDelegation -OfferName <String> -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="4338d-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="4338d-106">Get</span></span>
```
Get-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="4338d-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4338d-107">ResourceId</span></span>
```
Get-AzsOfferDelegation -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="4338d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4338d-108">DESCRIPTION</span></span>
<span data-ttu-id="4338d-109">Rufen Sie die Liste der Delegierten Angebote ab.</span><span class="sxs-lookup"><span data-stu-id="4338d-109">Get the list of delegated offers.</span></span>

## <span data-ttu-id="4338d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4338d-110">EXAMPLES</span></span>

### <span data-ttu-id="4338d-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4338d-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1
```

<span data-ttu-id="4338d-112">Rufen Sie die Liste der Delegierten Angebote ab.</span><span class="sxs-lookup"><span data-stu-id="4338d-112">Get the list of delegated offers.</span></span>

## <span data-ttu-id="4338d-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="4338d-113">PARAMETERS</span></span>

### <span data-ttu-id="4338d-114">-Name</span><span class="sxs-lookup"><span data-stu-id="4338d-114">-Name</span></span>
<span data-ttu-id="4338d-115">Der Name einer Angebots Delegation.</span><span class="sxs-lookup"><span data-stu-id="4338d-115">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="4338d-116">-Angebotname</span><span class="sxs-lookup"><span data-stu-id="4338d-116">-OfferName</span></span>
<span data-ttu-id="4338d-117">Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="4338d-117">Name of an offer.</span></span>

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

### <span data-ttu-id="4338d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4338d-118">-ResourceGroupName</span></span>
<span data-ttu-id="4338d-119">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="4338d-119">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="4338d-120">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4338d-120">-ResourceId</span></span>
<span data-ttu-id="4338d-121">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="4338d-121">The resource id.</span></span>

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

### <span data-ttu-id="4338d-122">-Skip</span><span class="sxs-lookup"><span data-stu-id="4338d-122">-Skip</span></span>
<span data-ttu-id="4338d-123">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="4338d-123">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="4338d-124">-Top</span><span class="sxs-lookup"><span data-stu-id="4338d-124">-Top</span></span>
<span data-ttu-id="4338d-125">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="4338d-125">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="4338d-126">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="4338d-126">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="4338d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4338d-127">CommonParameters</span></span>
<span data-ttu-id="4338d-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4338d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4338d-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4338d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4338d-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4338d-130">INPUTS</span></span>

## <span data-ttu-id="4338d-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4338d-131">OUTPUTS</span></span>

### <span data-ttu-id="4338d-132">Microsoft. AzureStack. Management. Subscriptions. admin. Models. OfferDelegation</span><span class="sxs-lookup"><span data-stu-id="4338d-132">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="4338d-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="4338d-133">NOTES</span></span>

## <span data-ttu-id="4338d-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4338d-134">RELATED LINKS</span></span>

