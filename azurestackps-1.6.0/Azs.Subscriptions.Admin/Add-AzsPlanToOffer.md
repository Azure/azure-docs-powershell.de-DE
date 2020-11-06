---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e501feeea3509725b53c85007934c8e682de48a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93474985"
---
# <span data-ttu-id="dabee-101">Add-AzsPlanToOffer</span><span class="sxs-lookup"><span data-stu-id="dabee-101">Add-AzsPlanToOffer</span></span>

## <span data-ttu-id="dabee-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dabee-102">SYNOPSIS</span></span>
<span data-ttu-id="dabee-103">Verknüpft einen Plan mit einem Angebot.</span><span class="sxs-lookup"><span data-stu-id="dabee-103">Links a plan to an offer.</span></span>

## <span data-ttu-id="dabee-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dabee-104">SYNTAX</span></span>

```
Add-AzsPlanToOffer [-PlanName] <String> [-OfferName] <String> [-ResourceGroupName] <String>
 [[-PlanLinkType] <String>] [[-MaxAcquisitionCount] <Int64>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dabee-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dabee-105">DESCRIPTION</span></span>
<span data-ttu-id="dabee-106">Verknüpft einen Plan mit einem Angebot.</span><span class="sxs-lookup"><span data-stu-id="dabee-106">Links a plan to an offer.</span></span>

## <span data-ttu-id="dabee-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dabee-107">EXAMPLES</span></span>

### <span data-ttu-id="dabee-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="dabee-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsPlanToOffer -PlanLinkType Addon -Offer offer1 -PlanName plan1 -ResourceGroupName rg1 -MaxAcquisitionCount 2
```

## <span data-ttu-id="dabee-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="dabee-109">PARAMETERS</span></span>

### <span data-ttu-id="dabee-110">-Force</span><span class="sxs-lookup"><span data-stu-id="dabee-110">-Force</span></span>
<span data-ttu-id="dabee-111">Kennzeichnen, um das Element ohne Bestätigung zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="dabee-111">Flag to remove the item without confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dabee-112">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="dabee-112">-MaxAcquisitionCount</span></span>
<span data-ttu-id="dabee-113">Die maximale Anzahl von Käufen durch Abonnenten</span><span class="sxs-lookup"><span data-stu-id="dabee-113">The maximum acquisition count by subscribers</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dabee-114">-Angebotname</span><span class="sxs-lookup"><span data-stu-id="dabee-114">-OfferName</span></span>
<span data-ttu-id="dabee-115">Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="dabee-115">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dabee-116">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="dabee-116">-PlanLinkType</span></span>
<span data-ttu-id="dabee-117">Der Typ des Plan Links.</span><span class="sxs-lookup"><span data-stu-id="dabee-117">Type of the plan link.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dabee-118">-Planname</span><span class="sxs-lookup"><span data-stu-id="dabee-118">-PlanName</span></span>
<span data-ttu-id="dabee-119">Der Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="dabee-119">Name of the plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dabee-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dabee-120">-ResourceGroupName</span></span>
<span data-ttu-id="dabee-121">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="dabee-121">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dabee-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dabee-122">-Confirm</span></span>
<span data-ttu-id="dabee-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dabee-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dabee-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dabee-124">-WhatIf</span></span>
<span data-ttu-id="dabee-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dabee-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dabee-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dabee-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dabee-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dabee-127">CommonParameters</span></span>
<span data-ttu-id="dabee-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dabee-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dabee-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dabee-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dabee-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dabee-130">INPUTS</span></span>

## <span data-ttu-id="dabee-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dabee-131">OUTPUTS</span></span>

## <span data-ttu-id="dabee-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="dabee-132">NOTES</span></span>

## <span data-ttu-id="dabee-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dabee-133">RELATED LINKS</span></span>

