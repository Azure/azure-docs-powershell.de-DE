---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25bd0c892c8c5978493d855246be994bc96158db
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840635"
---
# <span data-ttu-id="539c3-101">Set-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="539c3-101">Set-AzsSubscription</span></span>

## <span data-ttu-id="539c3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="539c3-102">SYNOPSIS</span></span>
<span data-ttu-id="539c3-103">Erstellen oder Aktualisieren eines Abonnements</span><span class="sxs-lookup"><span data-stu-id="539c3-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="539c3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="539c3-104">SYNTAX</span></span>

### <span data-ttu-id="539c3-105">Festlegen (Standard)</span><span class="sxs-lookup"><span data-stu-id="539c3-105">Set (Default)</span></span>
```
Set-AzsSubscription [-OfferId <String>] [-Type <String>]
 [-Tags <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -SubscriptionId <String>
 [-State <String>] [-TenantId <String>] [-DisplayName <String>] [-Location <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="539c3-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="539c3-106">ResourceId</span></span>
```
Set-AzsSubscription -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="539c3-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="539c3-107">InputObject</span></span>
```
Set-AzsSubscription -InputObject <SubscriptionModel> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="539c3-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="539c3-108">DESCRIPTION</span></span>
<span data-ttu-id="539c3-109">Erstellen oder Aktualisieren eines Abonnements</span><span class="sxs-lookup"><span data-stu-id="539c3-109">Create or updates a subscription.</span></span>

## <span data-ttu-id="539c3-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="539c3-110">EXAMPLES</span></span>

### <span data-ttu-id="539c3-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="539c3-111">EXAMPLE 1</span></span>
```
Set-AzsSubscription -SubscriptionId 2d9f5af9-3397-44fb-8700-d98762c2422a -DisplayName MyTestSub -State Enabled -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="539c3-112">Erstellen oder Aktualisieren eines Abonnements</span><span class="sxs-lookup"><span data-stu-id="539c3-112">Create or updates a subscription.</span></span>

## <span data-ttu-id="539c3-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="539c3-113">PARAMETERS</span></span>

### <span data-ttu-id="539c3-114">-Angebots-Nr</span><span class="sxs-lookup"><span data-stu-id="539c3-114">-OfferId</span></span>
<span data-ttu-id="539c3-115">Der Bezeichner des Angebots unter dem Bereich eines Delegierten Anbieters.</span><span class="sxs-lookup"><span data-stu-id="539c3-115">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="539c3-116">-Typ</span><span class="sxs-lookup"><span data-stu-id="539c3-116">-Type</span></span>
<span data-ttu-id="539c3-117">Der Typ der Ressource.</span><span class="sxs-lookup"><span data-stu-id="539c3-117">Type of resource.</span></span>

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

### <span data-ttu-id="539c3-118">-Tags</span><span class="sxs-lookup"><span data-stu-id="539c3-118">-Tags</span></span>
<span data-ttu-id="539c3-119">Liste der Schlüssel-Wert-Paare</span><span class="sxs-lookup"><span data-stu-id="539c3-119">List of key-value pairs.</span></span>

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

### <span data-ttu-id="539c3-120">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="539c3-120">-SubscriptionId</span></span>
<span data-ttu-id="539c3-121">Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="539c3-121">Subscription identifier.</span></span>

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

### <span data-ttu-id="539c3-122">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="539c3-122">-State</span></span>
<span data-ttu-id="539c3-123">Status des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="539c3-123">Subscription state.</span></span>

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

### <span data-ttu-id="539c3-124">-Mandanten-Nr</span><span class="sxs-lookup"><span data-stu-id="539c3-124">-TenantId</span></span>
<span data-ttu-id="539c3-125">Verzeichnis Mandanten-ID.</span><span class="sxs-lookup"><span data-stu-id="539c3-125">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="539c3-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="539c3-126">-DisplayName</span></span>
<span data-ttu-id="539c3-127">Name des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="539c3-127">Subscription name.</span></span>

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

### <span data-ttu-id="539c3-128">-Standort</span><span class="sxs-lookup"><span data-stu-id="539c3-128">-Location</span></span>
<span data-ttu-id="539c3-129">Ort, an dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="539c3-129">Location where resource is location.</span></span>

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

### <span data-ttu-id="539c3-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="539c3-130">-ResourceId</span></span>
<span data-ttu-id="539c3-131">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="539c3-131">The resource ID.</span></span>

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

### <span data-ttu-id="539c3-132">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="539c3-132">-InputObject</span></span>
<span data-ttu-id="539c3-133">Posbbily geändertes Netzwerk Kontingent, das von Get-AzsNetworkQuota zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="539c3-133">Posbbily modified network quota returned by Get-AzsNetworkQuota.</span></span>

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

### <span data-ttu-id="539c3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="539c3-134">-WhatIf</span></span>
<span data-ttu-id="539c3-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="539c3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="539c3-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="539c3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="539c3-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="539c3-137">-Confirm</span></span>
<span data-ttu-id="539c3-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="539c3-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="539c3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="539c3-139">CommonParameters</span></span>
<span data-ttu-id="539c3-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="539c3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="539c3-141">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="539c3-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="539c3-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="539c3-142">INPUTS</span></span>

## <span data-ttu-id="539c3-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="539c3-143">OUTPUTS</span></span>

### <span data-ttu-id="539c3-144">Microsoft. AzureStack. Management. Subscription. Models. SubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="539c3-144">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="539c3-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="539c3-145">NOTES</span></span>

## <span data-ttu-id="539c3-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="539c3-146">RELATED LINKS</span></span>
