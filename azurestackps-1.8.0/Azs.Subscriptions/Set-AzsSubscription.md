---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25bd0c892c8c5978493d855246be994bc96158db
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827448"
---
# <span data-ttu-id="a9479-101">Set-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="a9479-101">Set-AzsSubscription</span></span>

## <span data-ttu-id="a9479-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a9479-102">SYNOPSIS</span></span>
<span data-ttu-id="a9479-103">Erstellen oder Aktualisieren eines Abonnements</span><span class="sxs-lookup"><span data-stu-id="a9479-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="a9479-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9479-104">SYNTAX</span></span>

### <span data-ttu-id="a9479-105">Festlegen (Standard)</span><span class="sxs-lookup"><span data-stu-id="a9479-105">Set (Default)</span></span>
```
Set-AzsSubscription [-OfferId <String>] [-Type <String>]
 [-Tags <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -SubscriptionId <String>
 [-State <String>] [-TenantId <String>] [-DisplayName <String>] [-Location <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a9479-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9479-106">ResourceId</span></span>
```
Set-AzsSubscription -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9479-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="a9479-107">InputObject</span></span>
```
Set-AzsSubscription -InputObject <SubscriptionModel> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9479-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9479-108">DESCRIPTION</span></span>
<span data-ttu-id="a9479-109">Erstellen oder Aktualisieren eines Abonnements</span><span class="sxs-lookup"><span data-stu-id="a9479-109">Create or updates a subscription.</span></span>

## <span data-ttu-id="a9479-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a9479-110">EXAMPLES</span></span>

### <span data-ttu-id="a9479-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a9479-111">EXAMPLE 1</span></span>
```
Set-AzsSubscription -SubscriptionId 2d9f5af9-3397-44fb-8700-d98762c2422a -DisplayName MyTestSub -State Enabled -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="a9479-112">Erstellen oder Aktualisieren eines Abonnements</span><span class="sxs-lookup"><span data-stu-id="a9479-112">Create or updates a subscription.</span></span>

## <span data-ttu-id="a9479-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9479-113">PARAMETERS</span></span>

### <span data-ttu-id="a9479-114">-Angebots-Nr</span><span class="sxs-lookup"><span data-stu-id="a9479-114">-OfferId</span></span>
<span data-ttu-id="a9479-115">Der Bezeichner des Angebots unter dem Bereich eines Delegierten Anbieters.</span><span class="sxs-lookup"><span data-stu-id="a9479-115">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9479-116">-Typ</span><span class="sxs-lookup"><span data-stu-id="a9479-116">-Type</span></span>
<span data-ttu-id="a9479-117">Der Typ der Ressource.</span><span class="sxs-lookup"><span data-stu-id="a9479-117">Type of resource.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9479-118">-Tags</span><span class="sxs-lookup"><span data-stu-id="a9479-118">-Tags</span></span>
<span data-ttu-id="a9479-119">Liste der Schlüssel-Wert-Paare</span><span class="sxs-lookup"><span data-stu-id="a9479-119">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: Set
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9479-120">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="a9479-120">-SubscriptionId</span></span>
<span data-ttu-id="a9479-121">Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="a9479-121">Subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9479-122">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="a9479-122">-State</span></span>
<span data-ttu-id="a9479-123">Status des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="a9479-123">Subscription state.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9479-124">-Mandanten-Nr</span><span class="sxs-lookup"><span data-stu-id="a9479-124">-TenantId</span></span>
<span data-ttu-id="a9479-125">Verzeichnis Mandanten-ID.</span><span class="sxs-lookup"><span data-stu-id="a9479-125">Directory tenant identifier.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9479-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a9479-126">-DisplayName</span></span>
<span data-ttu-id="a9479-127">Name des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="a9479-127">Subscription name.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9479-128">-Standort</span><span class="sxs-lookup"><span data-stu-id="a9479-128">-Location</span></span>
<span data-ttu-id="a9479-129">Ort, an dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="a9479-129">Location where resource is location.</span></span>

```yaml
Type: String
Parameter Sets: Set
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9479-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a9479-130">-ResourceId</span></span>
<span data-ttu-id="a9479-131">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="a9479-131">The resource ID.</span></span>

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

### <span data-ttu-id="a9479-132">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a9479-132">-InputObject</span></span>
<span data-ttu-id="a9479-133">Posbbily geändertes Netzwerk Kontingent, das von Get-AzsNetworkQuota zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="a9479-133">Posbbily modified network quota returned by Get-AzsNetworkQuota.</span></span>

```yaml
Type: SubscriptionModel
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9479-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9479-134">-WhatIf</span></span>
<span data-ttu-id="a9479-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a9479-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9479-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a9479-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9479-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a9479-137">-Confirm</span></span>
<span data-ttu-id="a9479-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a9479-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9479-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9479-139">CommonParameters</span></span>
<span data-ttu-id="a9479-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9479-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9479-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9479-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9479-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a9479-142">INPUTS</span></span>

## <span data-ttu-id="a9479-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a9479-143">OUTPUTS</span></span>

### <span data-ttu-id="a9479-144">Microsoft. AzureStack. Management. Subscription. Models. SubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="a9479-144">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="a9479-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="a9479-145">NOTES</span></span>

## <span data-ttu-id="a9479-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a9479-146">RELATED LINKS</span></span>
