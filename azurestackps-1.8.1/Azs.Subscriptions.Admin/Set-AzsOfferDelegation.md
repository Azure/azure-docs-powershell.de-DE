---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1256fa41d7accc175e79bb531c62f76ace6482d8
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93828059"
---
# <span data-ttu-id="5e06c-101">Set-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="5e06c-101">Set-AzsOfferDelegation</span></span>

## <span data-ttu-id="5e06c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5e06c-102">SYNOPSIS</span></span>
<span data-ttu-id="5e06c-103">Aktualisiert die Angebots Delegierung.</span><span class="sxs-lookup"><span data-stu-id="5e06c-103">Updates the offer delegation.</span></span>

## <span data-ttu-id="5e06c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e06c-104">SYNTAX</span></span>

### <span data-ttu-id="5e06c-105">Update (Standard)</span><span class="sxs-lookup"><span data-stu-id="5e06c-105">Update (Default)</span></span>
```
Set-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e06c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="5e06c-106">InputObject</span></span>
```
Set-AzsOfferDelegation [-SubscriptionId <String>] [-Location <String>] -InputObject <OfferDelegation> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e06c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e06c-107">ResourceId</span></span>
```
Set-AzsOfferDelegation [-SubscriptionId <String>] -ResourceId <String> [-Location <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e06c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e06c-108">DESCRIPTION</span></span>
<span data-ttu-id="5e06c-109">Aktualisiert die Angebots Delegierung.</span><span class="sxs-lookup"><span data-stu-id="5e06c-109">Updates the offer delegation.</span></span>

## <span data-ttu-id="5e06c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5e06c-110">EXAMPLES</span></span>

### <span data-ttu-id="5e06c-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5e06c-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsOfferDelegation -Offer offer1 -ResourceGroupName rg1 -Name delegate1 -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946" -Location "local"
```

<span data-ttu-id="5e06c-112">Aktualisiert die Angebots Delegierung.</span><span class="sxs-lookup"><span data-stu-id="5e06c-112">Updates the offer delegation.</span></span>

## <span data-ttu-id="5e06c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e06c-113">PARAMETERS</span></span>

### <span data-ttu-id="5e06c-114">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5e06c-114">-InputObject</span></span>
<span data-ttu-id="5e06c-115">Das Eingabeobjekt vom Typ Microsoft. AzureStack. Management. Subscriptions. admin. Models. OfferDelegation.</span><span class="sxs-lookup"><span data-stu-id="5e06c-115">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation.</span></span>

```yaml
Type: OfferDelegation
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e06c-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="5e06c-116">-Location</span></span>
<span data-ttu-id="5e06c-117">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="5e06c-117">Location of the resource.</span></span>

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

### <span data-ttu-id="5e06c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="5e06c-118">-Name</span></span>
<span data-ttu-id="5e06c-119">Der Name einer Angebots Delegation.</span><span class="sxs-lookup"><span data-stu-id="5e06c-119">Name of a offer delegation.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e06c-120">-Angebotname</span><span class="sxs-lookup"><span data-stu-id="5e06c-120">-OfferName</span></span>
<span data-ttu-id="5e06c-121">Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="5e06c-121">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e06c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e06c-122">-ResourceGroupName</span></span>
<span data-ttu-id="5e06c-123">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="5e06c-123">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e06c-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5e06c-124">-ResourceId</span></span>
<span data-ttu-id="5e06c-125">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="5e06c-125">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e06c-126">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="5e06c-126">-SubscriptionId</span></span>
<span data-ttu-id="5e06c-127">Der Bezeichner des Abonnements, das das Delegierte Angebot erhält.</span><span class="sxs-lookup"><span data-stu-id="5e06c-127">Identifier of the subscription receiving the delegated offer.</span></span>

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

### <span data-ttu-id="5e06c-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5e06c-128">-Confirm</span></span>
<span data-ttu-id="5e06c-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5e06c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e06c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e06c-130">-WhatIf</span></span>
<span data-ttu-id="5e06c-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e06c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e06c-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5e06c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e06c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e06c-133">CommonParameters</span></span>
<span data-ttu-id="5e06c-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e06c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e06c-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e06c-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e06c-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5e06c-136">INPUTS</span></span>

## <span data-ttu-id="5e06c-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5e06c-137">OUTPUTS</span></span>

### <span data-ttu-id="5e06c-138">Microsoft. AzureStack. Management. Subscriptions. admin. Models. OfferDelegation</span><span class="sxs-lookup"><span data-stu-id="5e06c-138">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.OfferDelegation</span></span>

## <span data-ttu-id="5e06c-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="5e06c-139">NOTES</span></span>

## <span data-ttu-id="5e06c-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5e06c-140">RELATED LINKS</span></span>

