---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3a4c99f48087dcbac17dc10da3c647525670fe90
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827831"
---
# <span data-ttu-id="0106b-101">New-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="0106b-101">New-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="0106b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0106b-102">SYNOPSIS</span></span>
<span data-ttu-id="0106b-103">Erstellt einen Abonnementplan.</span><span class="sxs-lookup"><span data-stu-id="0106b-103">Creates a subscription plan.</span></span>

## <span data-ttu-id="0106b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0106b-104">SYNTAX</span></span>

```
New-AzsSubscriptionPlan [[-AcquisitionId] <Guid>] [-PlanId] <String> [-TargetSubscriptionId] <Guid> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0106b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0106b-105">DESCRIPTION</span></span>
<span data-ttu-id="0106b-106">Erstellt einen Abonnementplan.</span><span class="sxs-lookup"><span data-stu-id="0106b-106">Creates a subscription plan.</span></span>

## <span data-ttu-id="0106b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0106b-107">EXAMPLES</span></span>

### <span data-ttu-id="0106b-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0106b-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsSubscriptionPlan -PlanId "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/plans/plan1" -AcquisitionId $([Guid]::NewGuid()) -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="0106b-109">Erstellen Sie einen Abonnementplan.</span><span class="sxs-lookup"><span data-stu-id="0106b-109">Create an subscription plan.</span></span>

## <span data-ttu-id="0106b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0106b-110">PARAMETERS</span></span>

### <span data-ttu-id="0106b-111">-Akquisitions-Nr.</span><span class="sxs-lookup"><span data-stu-id="0106b-111">-AcquisitionId</span></span>
<span data-ttu-id="0106b-112">Akquisitions-ID.</span><span class="sxs-lookup"><span data-stu-id="0106b-112">Acquisition identifier.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: $([Guid]::NewGuid())
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0106b-113">-Plan-Nr.</span><span class="sxs-lookup"><span data-stu-id="0106b-113">-PlanId</span></span>
<span data-ttu-id="0106b-114">Plan-ID im Kontext des Mandanten Abonnements</span><span class="sxs-lookup"><span data-stu-id="0106b-114">Plan identifier in the tenant subscription context.</span></span>

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

### <span data-ttu-id="0106b-115">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0106b-115">-TargetSubscriptionId</span></span>
<span data-ttu-id="0106b-116">Die zielabonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="0106b-116">The target subscription ID.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0106b-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0106b-117">-Confirm</span></span>
<span data-ttu-id="0106b-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0106b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0106b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0106b-119">-WhatIf</span></span>
<span data-ttu-id="0106b-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0106b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0106b-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0106b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0106b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0106b-122">CommonParameters</span></span>
<span data-ttu-id="0106b-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0106b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0106b-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0106b-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0106b-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0106b-125">INPUTS</span></span>

## <span data-ttu-id="0106b-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0106b-126">OUTPUTS</span></span>

### <span data-ttu-id="0106b-127">Microsoft. AzureStack. Management. Subscriptions. admin. Models. PlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="0106b-127">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.PlanAcquisition</span></span>

## <span data-ttu-id="0106b-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="0106b-128">NOTES</span></span>

## <span data-ttu-id="0106b-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0106b-129">RELATED LINKS</span></span>

