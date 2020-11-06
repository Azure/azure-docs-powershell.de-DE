---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0ec978cebfaa12f574ce20638347839fd70099df
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475457"
---
# <span data-ttu-id="783b9-101">Remove-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="783b9-101">Remove-AzsOfferDelegation</span></span>

## <span data-ttu-id="783b9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="783b9-102">SYNOPSIS</span></span>
<span data-ttu-id="783b9-103">Entfernt die Angebots Delegierung</span><span class="sxs-lookup"><span data-stu-id="783b9-103">Removes the offer delegation</span></span>

## <span data-ttu-id="783b9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="783b9-104">SYNTAX</span></span>

### <span data-ttu-id="783b9-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="783b9-105">Delete (Default)</span></span>
```
Remove-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="783b9-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="783b9-106">ResourceId</span></span>
```
Remove-AzsOfferDelegation -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="783b9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="783b9-107">DESCRIPTION</span></span>
<span data-ttu-id="783b9-108">Entfernt die Angebots Delegierung</span><span class="sxs-lookup"><span data-stu-id="783b9-108">Removes the offer delegation</span></span>

## <span data-ttu-id="783b9-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="783b9-109">EXAMPLES</span></span>

### <span data-ttu-id="783b9-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="783b9-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegation1
```

<span data-ttu-id="783b9-111">Entfernt die Angebots Delegierung</span><span class="sxs-lookup"><span data-stu-id="783b9-111">Removes the offer delegation</span></span>

## <span data-ttu-id="783b9-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="783b9-112">PARAMETERS</span></span>

### <span data-ttu-id="783b9-113">-Force</span><span class="sxs-lookup"><span data-stu-id="783b9-113">-Force</span></span>
<span data-ttu-id="783b9-114">Kennzeichnen, um das Element ohne Bestätigung zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="783b9-114">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="783b9-115">-Name</span><span class="sxs-lookup"><span data-stu-id="783b9-115">-Name</span></span>
<span data-ttu-id="783b9-116">Der Name einer Angebots Delegation.</span><span class="sxs-lookup"><span data-stu-id="783b9-116">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="783b9-117">-Angebotname</span><span class="sxs-lookup"><span data-stu-id="783b9-117">-OfferName</span></span>
<span data-ttu-id="783b9-118">Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="783b9-118">Name of an offer.</span></span>

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

### <span data-ttu-id="783b9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="783b9-119">-ResourceGroupName</span></span>
<span data-ttu-id="783b9-120">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="783b9-120">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="783b9-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="783b9-121">-ResourceId</span></span>
<span data-ttu-id="783b9-122">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="783b9-122">The resource id.</span></span>

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

### <span data-ttu-id="783b9-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="783b9-123">-Confirm</span></span>
<span data-ttu-id="783b9-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="783b9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="783b9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="783b9-125">-WhatIf</span></span>
<span data-ttu-id="783b9-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="783b9-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="783b9-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="783b9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="783b9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="783b9-128">CommonParameters</span></span>
<span data-ttu-id="783b9-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="783b9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="783b9-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="783b9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="783b9-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="783b9-131">INPUTS</span></span>

## <span data-ttu-id="783b9-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="783b9-132">OUTPUTS</span></span>

## <span data-ttu-id="783b9-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="783b9-133">NOTES</span></span>

## <span data-ttu-id="783b9-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="783b9-134">RELATED LINKS</span></span>

