---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e9fc37b5f99a9ad38e92ce1efc730718882b533d
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94006952"
---
# <span data-ttu-id="fd99f-101">Remove-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="fd99f-101">Remove-AzsOfferDelegation</span></span>

## <span data-ttu-id="fd99f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fd99f-102">SYNOPSIS</span></span>
<span data-ttu-id="fd99f-103">Entfernt die Angebots Delegierung</span><span class="sxs-lookup"><span data-stu-id="fd99f-103">Removes the offer delegation</span></span>

## <span data-ttu-id="fd99f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd99f-104">SYNTAX</span></span>

### <span data-ttu-id="fd99f-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="fd99f-105">Delete (Default)</span></span>
```
Remove-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd99f-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd99f-106">ResourceId</span></span>
```
Remove-AzsOfferDelegation -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd99f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fd99f-107">DESCRIPTION</span></span>
<span data-ttu-id="fd99f-108">Entfernt die Angebots Delegierung</span><span class="sxs-lookup"><span data-stu-id="fd99f-108">Removes the offer delegation</span></span>

## <span data-ttu-id="fd99f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fd99f-109">EXAMPLES</span></span>

### <span data-ttu-id="fd99f-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="fd99f-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegation1
```

<span data-ttu-id="fd99f-111">Entfernt die Angebots Delegierung</span><span class="sxs-lookup"><span data-stu-id="fd99f-111">Removes the offer delegation</span></span>

## <span data-ttu-id="fd99f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd99f-112">PARAMETERS</span></span>

### <span data-ttu-id="fd99f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="fd99f-113">-Force</span></span>
<span data-ttu-id="fd99f-114">Kennzeichnen, um das Element ohne Bestätigung zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="fd99f-114">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="fd99f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="fd99f-115">-Name</span></span>
<span data-ttu-id="fd99f-116">Der Name einer Angebots Delegation.</span><span class="sxs-lookup"><span data-stu-id="fd99f-116">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="fd99f-117">-Angebotname</span><span class="sxs-lookup"><span data-stu-id="fd99f-117">-OfferName</span></span>
<span data-ttu-id="fd99f-118">Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="fd99f-118">Name of an offer.</span></span>

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

### <span data-ttu-id="fd99f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd99f-119">-ResourceGroupName</span></span>
<span data-ttu-id="fd99f-120">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="fd99f-120">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="fd99f-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="fd99f-121">-ResourceId</span></span>
<span data-ttu-id="fd99f-122">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="fd99f-122">The resource id.</span></span>

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

### <span data-ttu-id="fd99f-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fd99f-123">-Confirm</span></span>
<span data-ttu-id="fd99f-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fd99f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd99f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd99f-125">-WhatIf</span></span>
<span data-ttu-id="fd99f-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fd99f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd99f-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fd99f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd99f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd99f-128">CommonParameters</span></span>
<span data-ttu-id="fd99f-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd99f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd99f-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd99f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd99f-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fd99f-131">INPUTS</span></span>

## <span data-ttu-id="fd99f-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fd99f-132">OUTPUTS</span></span>

## <span data-ttu-id="fd99f-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="fd99f-133">NOTES</span></span>

## <span data-ttu-id="fd99f-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fd99f-134">RELATED LINKS</span></span>

