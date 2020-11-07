---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b82dadf9a9e26b0023872378d41e4978e18436ab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93662002"
---
# <span data-ttu-id="829f4-101">Remove-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="829f4-101">Remove-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="829f4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="829f4-102">SYNOPSIS</span></span>
<span data-ttu-id="829f4-103">Löscht einen Abonnementplan.</span><span class="sxs-lookup"><span data-stu-id="829f4-103">Deletes a subscription plan.</span></span>

## <span data-ttu-id="829f4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="829f4-104">SYNTAX</span></span>

### <span data-ttu-id="829f4-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="829f4-105">Delete (Default)</span></span>
```
Remove-AzsSubscriptionPlan -AcquisitionId <Guid> -TargetSubscriptionId <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="829f4-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="829f4-106">ResourceId</span></span>
```
Remove-AzsSubscriptionPlan -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="829f4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="829f4-107">DESCRIPTION</span></span>
<span data-ttu-id="829f4-108">Löscht einen Abonnementplan.</span><span class="sxs-lookup"><span data-stu-id="829f4-108">Deletes a subscription plan.</span></span>

## <span data-ttu-id="829f4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="829f4-109">EXAMPLES</span></span>

### <span data-ttu-id="829f4-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="829f4-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsSubscriptionPlan -AcquisitionId $([Guid]::NewGuid()) -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="829f4-111">Löschen eines Abonnementplans</span><span class="sxs-lookup"><span data-stu-id="829f4-111">Delete a subscription plan.</span></span>

## <span data-ttu-id="829f4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="829f4-112">PARAMETERS</span></span>

### <span data-ttu-id="829f4-113">-Akquisitions-Nr.</span><span class="sxs-lookup"><span data-stu-id="829f4-113">-AcquisitionId</span></span>
<span data-ttu-id="829f4-114">Der Plan Erfassung-Bezeichner</span><span class="sxs-lookup"><span data-stu-id="829f4-114">The plan acquisition Identifier</span></span>

```yaml
Type: Guid
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="829f4-115">-Force</span><span class="sxs-lookup"><span data-stu-id="829f4-115">-Force</span></span>
<span data-ttu-id="829f4-116">Kennzeichnen, um das Element ohne Bestätigung zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="829f4-116">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="829f4-117">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="829f4-117">-ResourceId</span></span>
<span data-ttu-id="829f4-118">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="829f4-118">The resource id.</span></span>

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

### <span data-ttu-id="829f4-119">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="829f4-119">-TargetSubscriptionId</span></span>
<span data-ttu-id="829f4-120">Die zielabonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="829f4-120">The target subscription ID.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="829f4-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="829f4-121">-Confirm</span></span>
<span data-ttu-id="829f4-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="829f4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="829f4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="829f4-123">-WhatIf</span></span>
<span data-ttu-id="829f4-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="829f4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="829f4-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="829f4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="829f4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="829f4-126">CommonParameters</span></span>
<span data-ttu-id="829f4-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="829f4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="829f4-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="829f4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="829f4-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="829f4-129">INPUTS</span></span>

## <span data-ttu-id="829f4-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="829f4-130">OUTPUTS</span></span>

## <span data-ttu-id="829f4-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="829f4-131">NOTES</span></span>

## <span data-ttu-id="829f4-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="829f4-132">RELATED LINKS</span></span>

