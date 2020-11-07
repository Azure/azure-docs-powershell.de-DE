---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b2cb2886e84b42d499fb04693757cee333458f9b
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827863"
---
# <span data-ttu-id="7bc45-101">Get-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="7bc45-101">Get-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="7bc45-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7bc45-102">SYNOPSIS</span></span>
<span data-ttu-id="7bc45-103">Abrufen einer Sammlung aller erworbenen Pläne, auf die das Abonnement zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="7bc45-103">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="7bc45-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7bc45-104">SYNTAX</span></span>

### <span data-ttu-id="7bc45-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="7bc45-105">List (Default)</span></span>
```
Get-AzsSubscriptionPlan -TargetSubscriptionId <Guid> [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="7bc45-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="7bc45-106">Get</span></span>
```
Get-AzsSubscriptionPlan -AcquisitionId <Guid> -TargetSubscriptionId <Guid> [<CommonParameters>]
```

### <span data-ttu-id="7bc45-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7bc45-107">ResourceId</span></span>
```
Get-AzsSubscriptionPlan -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="7bc45-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7bc45-108">DESCRIPTION</span></span>
<span data-ttu-id="7bc45-109">Abrufen einer Sammlung aller erworbenen Pläne, auf die das Abonnement zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="7bc45-109">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="7bc45-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7bc45-110">EXAMPLES</span></span>

### <span data-ttu-id="7bc45-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7bc45-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSubscriptionPlan -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="7bc45-112">Abrufen einer Sammlung aller erworbenen Pläne, auf die das Abonnement zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="7bc45-112">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="7bc45-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="7bc45-113">PARAMETERS</span></span>

### <span data-ttu-id="7bc45-114">-Akquisitions-Nr.</span><span class="sxs-lookup"><span data-stu-id="7bc45-114">-AcquisitionId</span></span>
<span data-ttu-id="7bc45-115">Der Plan Erfassung-Bezeichner</span><span class="sxs-lookup"><span data-stu-id="7bc45-115">The plan acquisition Identifier</span></span>

```yaml
Type: Guid
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bc45-116">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="7bc45-116">-ResourceId</span></span>
<span data-ttu-id="7bc45-117">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="7bc45-117">The resource id.</span></span>

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

### <span data-ttu-id="7bc45-118">-Skip</span><span class="sxs-lookup"><span data-stu-id="7bc45-118">-Skip</span></span>
<span data-ttu-id="7bc45-119">Überspringen Sie die ersten N Elemente, wie durch den Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="7bc45-119">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="7bc45-120">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7bc45-120">-TargetSubscriptionId</span></span>
<span data-ttu-id="7bc45-121">Die zielabonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="7bc45-121">The target subscription ID.</span></span>

```yaml
Type: Guid
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bc45-122">-Top</span><span class="sxs-lookup"><span data-stu-id="7bc45-122">-Top</span></span>
<span data-ttu-id="7bc45-123">Geben Sie die obersten N Elemente wie durch den Parameterwert angegeben zurück.</span><span class="sxs-lookup"><span data-stu-id="7bc45-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="7bc45-124">Gilt nach dem-Skip-Parameter.</span><span class="sxs-lookup"><span data-stu-id="7bc45-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="7bc45-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bc45-125">CommonParameters</span></span>
<span data-ttu-id="7bc45-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bc45-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bc45-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bc45-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bc45-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7bc45-128">INPUTS</span></span>

## <span data-ttu-id="7bc45-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7bc45-129">OUTPUTS</span></span>

### <span data-ttu-id="7bc45-130">Microsoft. AzureStack. Management. Subscriptions. admin. Models. PlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="7bc45-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.PlanAcquisition</span></span>

## <span data-ttu-id="7bc45-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="7bc45-131">NOTES</span></span>

## <span data-ttu-id="7bc45-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7bc45-132">RELATED LINKS</span></span>

