---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5f5c0050f6a1e226f5b5513e11d70fac1844ecda
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93828080"
---
# <span data-ttu-id="7f0b0-101">Remove-AzsPlanFromOffer</span><span class="sxs-lookup"><span data-stu-id="7f0b0-101">Remove-AzsPlanFromOffer</span></span>

## <span data-ttu-id="7f0b0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7f0b0-102">SYNOPSIS</span></span>
<span data-ttu-id="7f0b0-103">Aufheben der Verknüpfung zwischen einem Plan und einem Angebot</span><span class="sxs-lookup"><span data-stu-id="7f0b0-103">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="7f0b0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f0b0-104">SYNTAX</span></span>

```
Remove-AzsPlanFromOffer -PlanName <String> -OfferName <String> -ResourceGroupName <String>
 [-PlanLinkType <String>] [-MaxAcquisitionCount <Int64>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f0b0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f0b0-105">DESCRIPTION</span></span>
<span data-ttu-id="7f0b0-106">Aufheben der Verknüpfung zwischen einem Plan und einem Angebot</span><span class="sxs-lookup"><span data-stu-id="7f0b0-106">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="7f0b0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7f0b0-107">EXAMPLES</span></span>

### <span data-ttu-id="7f0b0-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7f0b0-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsPlanToOffer -Offer offer1 -PlanName plan1 -ResourceGroup rg1
```

## <span data-ttu-id="7f0b0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f0b0-109">PARAMETERS</span></span>

### <span data-ttu-id="7f0b0-110">-Force</span><span class="sxs-lookup"><span data-stu-id="7f0b0-110">-Force</span></span>
<span data-ttu-id="7f0b0-111">Kennzeichnen, um das Element ohne Bestätigung zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="7f0b0-111">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="7f0b0-112">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="7f0b0-112">-MaxAcquisitionCount</span></span>
<span data-ttu-id="7f0b0-113">Die maximale Anzahl von Käufen durch Abonnenten</span><span class="sxs-lookup"><span data-stu-id="7f0b0-113">The maximum acquisition count by subscribers</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f0b0-114">-Angebotname</span><span class="sxs-lookup"><span data-stu-id="7f0b0-114">-OfferName</span></span>
<span data-ttu-id="7f0b0-115">Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="7f0b0-115">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f0b0-116">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="7f0b0-116">-PlanLinkType</span></span>
<span data-ttu-id="7f0b0-117">Der Typ des Plan Links.</span><span class="sxs-lookup"><span data-stu-id="7f0b0-117">Type of the plan link.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f0b0-118">-Planname</span><span class="sxs-lookup"><span data-stu-id="7f0b0-118">-PlanName</span></span>
<span data-ttu-id="7f0b0-119">Der Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="7f0b0-119">Name of the plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f0b0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f0b0-120">-ResourceGroupName</span></span>
<span data-ttu-id="7f0b0-121">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="7f0b0-121">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f0b0-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7f0b0-122">-Confirm</span></span>
<span data-ttu-id="7f0b0-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7f0b0-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f0b0-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f0b0-124">-WhatIf</span></span>
<span data-ttu-id="7f0b0-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7f0b0-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f0b0-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7f0b0-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f0b0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f0b0-127">CommonParameters</span></span>
<span data-ttu-id="7f0b0-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f0b0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f0b0-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f0b0-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f0b0-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7f0b0-130">INPUTS</span></span>

## <span data-ttu-id="7f0b0-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7f0b0-131">OUTPUTS</span></span>

## <span data-ttu-id="7f0b0-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="7f0b0-132">NOTES</span></span>

## <span data-ttu-id="7f0b0-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7f0b0-133">RELATED LINKS</span></span>

