---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: 617a7ac7d949eb54ab08b0d0cb06c0fca3ba79bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475225"
---
# <span data-ttu-id="abecd-101">New-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="abecd-101">New-AzsSubscription</span></span>

## <span data-ttu-id="abecd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="abecd-102">SYNOPSIS</span></span>
<span data-ttu-id="abecd-103">Erstellen Sie ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="abecd-103">Create a subscription.</span></span>

## <span data-ttu-id="abecd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="abecd-104">SYNTAX</span></span>

```
New-AzsSubscription [-OfferId] <String> [[-DisplayName] <String>] [[-TenantId] <String>]
 [[-SubscriptionId] <String>] [[-State] <String>] [[-Location] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="abecd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="abecd-105">DESCRIPTION</span></span>
<span data-ttu-id="abecd-106">Erstellen Sie ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="abecd-106">Create a subscription.</span></span>

## <span data-ttu-id="abecd-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="abecd-107">EXAMPLES</span></span>

### <span data-ttu-id="abecd-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="abecd-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsSubscription -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="abecd-109">Erstellen Sie ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="abecd-109">Create a subscription.</span></span>

## <span data-ttu-id="abecd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="abecd-110">PARAMETERS</span></span>

### <span data-ttu-id="abecd-111">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="abecd-111">-DisplayName</span></span>
<span data-ttu-id="abecd-112">Name des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="abecd-112">Subscription name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abecd-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="abecd-113">-Location</span></span>
<span data-ttu-id="abecd-114">Ort, an dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="abecd-114">Location where resource is location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ArmLocation

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abecd-115">-Angebots-Nr</span><span class="sxs-lookup"><span data-stu-id="abecd-115">-OfferId</span></span>
<span data-ttu-id="abecd-116">Der Bezeichner des Angebots unter dem Bereich eines Delegierten Anbieters.</span><span class="sxs-lookup"><span data-stu-id="abecd-116">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abecd-117">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="abecd-117">-State</span></span>
<span data-ttu-id="abecd-118">Status des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="abecd-118">Subscription state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: Enabled
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abecd-119">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="abecd-119">-SubscriptionId</span></span>
<span data-ttu-id="abecd-120">Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="abecd-120">Subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abecd-121">-Mandanten-Nr</span><span class="sxs-lookup"><span data-stu-id="abecd-121">-TenantId</span></span>
<span data-ttu-id="abecd-122">Verzeichnis Mandanten-ID.</span><span class="sxs-lookup"><span data-stu-id="abecd-122">Directory tenant identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abecd-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="abecd-123">-Confirm</span></span>
<span data-ttu-id="abecd-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="abecd-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abecd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abecd-125">-WhatIf</span></span>
<span data-ttu-id="abecd-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="abecd-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abecd-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="abecd-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abecd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abecd-128">CommonParameters</span></span>
<span data-ttu-id="abecd-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abecd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abecd-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abecd-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abecd-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="abecd-131">INPUTS</span></span>

## <span data-ttu-id="abecd-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="abecd-132">OUTPUTS</span></span>

### <span data-ttu-id="abecd-133">Microsoft. AzureStack. Management. Subscription. Models. SubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="abecd-133">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="abecd-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="abecd-134">NOTES</span></span>

## <span data-ttu-id="abecd-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="abecd-135">RELATED LINKS</span></span>

