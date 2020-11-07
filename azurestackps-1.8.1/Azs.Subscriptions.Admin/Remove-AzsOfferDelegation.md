---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e9fc37b5f99a9ad38e92ce1efc730718882b533d
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93828091"
---
# <span data-ttu-id="8b4f7-101">Remove-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="8b4f7-101">Remove-AzsOfferDelegation</span></span>

## <span data-ttu-id="8b4f7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8b4f7-102">SYNOPSIS</span></span>
<span data-ttu-id="8b4f7-103">Entfernt die Angebots Delegierung</span><span class="sxs-lookup"><span data-stu-id="8b4f7-103">Removes the offer delegation</span></span>

## <span data-ttu-id="8b4f7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b4f7-104">SYNTAX</span></span>

### <span data-ttu-id="8b4f7-105">Löschen (Standard)</span><span class="sxs-lookup"><span data-stu-id="8b4f7-105">Delete (Default)</span></span>
```
Remove-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b4f7-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b4f7-106">ResourceId</span></span>
```
Remove-AzsOfferDelegation -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b4f7-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b4f7-107">DESCRIPTION</span></span>
<span data-ttu-id="8b4f7-108">Entfernt die Angebots Delegierung</span><span class="sxs-lookup"><span data-stu-id="8b4f7-108">Removes the offer delegation</span></span>

## <span data-ttu-id="8b4f7-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8b4f7-109">EXAMPLES</span></span>

### <span data-ttu-id="8b4f7-110">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8b4f7-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegation1
```

<span data-ttu-id="8b4f7-111">Entfernt die Angebots Delegierung</span><span class="sxs-lookup"><span data-stu-id="8b4f7-111">Removes the offer delegation</span></span>

## <span data-ttu-id="8b4f7-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b4f7-112">PARAMETERS</span></span>

### <span data-ttu-id="8b4f7-113">-Force</span><span class="sxs-lookup"><span data-stu-id="8b4f7-113">-Force</span></span>
<span data-ttu-id="8b4f7-114">Kennzeichnen, um das Element ohne Bestätigung zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="8b4f7-114">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="8b4f7-115">-Name</span><span class="sxs-lookup"><span data-stu-id="8b4f7-115">-Name</span></span>
<span data-ttu-id="8b4f7-116">Der Name einer Angebots Delegation.</span><span class="sxs-lookup"><span data-stu-id="8b4f7-116">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="8b4f7-117">-Angebotname</span><span class="sxs-lookup"><span data-stu-id="8b4f7-117">-OfferName</span></span>
<span data-ttu-id="8b4f7-118">Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="8b4f7-118">Name of an offer.</span></span>

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

### <span data-ttu-id="8b4f7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b4f7-119">-ResourceGroupName</span></span>
<span data-ttu-id="8b4f7-120">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="8b4f7-120">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="8b4f7-121">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="8b4f7-121">-ResourceId</span></span>
<span data-ttu-id="8b4f7-122">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="8b4f7-122">The resource id.</span></span>

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

### <span data-ttu-id="8b4f7-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8b4f7-123">-Confirm</span></span>
<span data-ttu-id="8b4f7-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8b4f7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b4f7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b4f7-125">-WhatIf</span></span>
<span data-ttu-id="8b4f7-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8b4f7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b4f7-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8b4f7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b4f7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b4f7-128">CommonParameters</span></span>
<span data-ttu-id="8b4f7-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b4f7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b4f7-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b4f7-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b4f7-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8b4f7-131">INPUTS</span></span>

## <span data-ttu-id="8b4f7-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8b4f7-132">OUTPUTS</span></span>

## <span data-ttu-id="8b4f7-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="8b4f7-133">NOTES</span></span>

## <span data-ttu-id="8b4f7-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8b4f7-134">RELATED LINKS</span></span>

