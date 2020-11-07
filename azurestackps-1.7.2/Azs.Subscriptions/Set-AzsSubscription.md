---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb23765090b0edfd14fa355b9809a2385900396e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93827380"
---
# <span data-ttu-id="52fb6-101">Set-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="52fb6-101">Set-AzsSubscription</span></span>

## <span data-ttu-id="52fb6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="52fb6-102">SYNOPSIS</span></span>
<span data-ttu-id="52fb6-103">Erstellen oder Aktualisieren eines Abonnements</span><span class="sxs-lookup"><span data-stu-id="52fb6-103">Create or updates a subscription.</span></span>

## <span data-ttu-id="52fb6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="52fb6-104">SYNTAX</span></span>

### <span data-ttu-id="52fb6-105">Festlegen (Standard)</span><span class="sxs-lookup"><span data-stu-id="52fb6-105">Set (Default)</span></span>
```
Set-AzsSubscription [-OfferId <String>] [-Type <String>]
 [-Tags <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -SubscriptionId <String>
 [-State <String>] [-TenantId <String>] [-DisplayName <String>] [-Location <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="52fb6-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="52fb6-106">ResourceId</span></span>
```
Set-AzsSubscription -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52fb6-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="52fb6-107">InputObject</span></span>
```
Set-AzsSubscription -InputObject <SubscriptionModel> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52fb6-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="52fb6-108">DESCRIPTION</span></span>
<span data-ttu-id="52fb6-109">Erstellen oder Aktualisieren eines Abonnements</span><span class="sxs-lookup"><span data-stu-id="52fb6-109">Create or updates a subscription.</span></span>

## <span data-ttu-id="52fb6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="52fb6-110">EXAMPLES</span></span>

### <span data-ttu-id="52fb6-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="52fb6-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsSubscription -SubscriptionId 2d9f5af9-3397-44fb-8700-d98762c2422a -DisplayName MyTestSub -State Enabled -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="52fb6-112">Erstellen oder Aktualisieren eines Abonnements</span><span class="sxs-lookup"><span data-stu-id="52fb6-112">Create or updates a subscription.</span></span>

## <span data-ttu-id="52fb6-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="52fb6-113">PARAMETERS</span></span>

### <span data-ttu-id="52fb6-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="52fb6-114">-DisplayName</span></span>
<span data-ttu-id="52fb6-115">Name des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="52fb6-115">Subscription name.</span></span>

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

### <span data-ttu-id="52fb6-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="52fb6-116">-InputObject</span></span>
<span data-ttu-id="52fb6-117">Posbbily geändertes Netzwerk Kontingent, das von Get-AzsNetworkQuota zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="52fb6-117">Posbbily modified network quota returned by Get-AzsNetworkQuota.</span></span>

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

### <span data-ttu-id="52fb6-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="52fb6-118">-Location</span></span>
<span data-ttu-id="52fb6-119">Ort, an dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="52fb6-119">Location where resource is location.</span></span>

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

### <span data-ttu-id="52fb6-120">-Angebots-Nr</span><span class="sxs-lookup"><span data-stu-id="52fb6-120">-OfferId</span></span>
<span data-ttu-id="52fb6-121">Der Bezeichner des Angebots unter dem Bereich eines Delegierten Anbieters.</span><span class="sxs-lookup"><span data-stu-id="52fb6-121">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="52fb6-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="52fb6-122">-ResourceId</span></span>
<span data-ttu-id="52fb6-123">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="52fb6-123">The resource ID.</span></span>

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

### <span data-ttu-id="52fb6-124">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="52fb6-124">-State</span></span>
<span data-ttu-id="52fb6-125">Status des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="52fb6-125">Subscription state.</span></span>

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

### <span data-ttu-id="52fb6-126">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="52fb6-126">-SubscriptionId</span></span>
<span data-ttu-id="52fb6-127">Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="52fb6-127">Subscription identifier.</span></span>

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

### <span data-ttu-id="52fb6-128">-Tags</span><span class="sxs-lookup"><span data-stu-id="52fb6-128">-Tags</span></span>
<span data-ttu-id="52fb6-129">Liste der Schlüssel-Wert-Paare</span><span class="sxs-lookup"><span data-stu-id="52fb6-129">List of key-value pairs.</span></span>

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

### <span data-ttu-id="52fb6-130">-Mandanten-Nr</span><span class="sxs-lookup"><span data-stu-id="52fb6-130">-TenantId</span></span>
<span data-ttu-id="52fb6-131">Verzeichnis Mandanten-ID.</span><span class="sxs-lookup"><span data-stu-id="52fb6-131">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="52fb6-132">-Typ</span><span class="sxs-lookup"><span data-stu-id="52fb6-132">-Type</span></span>
<span data-ttu-id="52fb6-133">Der Typ der Ressource.</span><span class="sxs-lookup"><span data-stu-id="52fb6-133">Type of resource.</span></span>

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

### <span data-ttu-id="52fb6-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="52fb6-134">-Confirm</span></span>
<span data-ttu-id="52fb6-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="52fb6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52fb6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52fb6-136">-WhatIf</span></span>
<span data-ttu-id="52fb6-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="52fb6-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52fb6-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="52fb6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52fb6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52fb6-139">CommonParameters</span></span>
<span data-ttu-id="52fb6-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52fb6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52fb6-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52fb6-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52fb6-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="52fb6-142">INPUTS</span></span>

## <span data-ttu-id="52fb6-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="52fb6-143">OUTPUTS</span></span>

### <span data-ttu-id="52fb6-144">Microsoft. AzureStack. Management. Subscription. Models. SubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="52fb6-144">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="52fb6-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="52fb6-145">NOTES</span></span>

## <span data-ttu-id="52fb6-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="52fb6-146">RELATED LINKS</span></span>

