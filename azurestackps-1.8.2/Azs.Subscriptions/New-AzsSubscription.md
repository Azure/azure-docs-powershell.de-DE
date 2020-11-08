---
external help file: Azs.Subscriptions-help.xml
Module Name: Azs.Subscriptions
online version: ''
schema: 2.0.0
ms.openlocfilehash: d905159ca62f34584f045a699621f6672507ffe1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007153"
---
# <span data-ttu-id="c0430-101">New-AzsSubscription</span><span class="sxs-lookup"><span data-stu-id="c0430-101">New-AzsSubscription</span></span>

## <span data-ttu-id="c0430-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c0430-102">SYNOPSIS</span></span>
<span data-ttu-id="c0430-103">Erstellen Sie ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c0430-103">Create a subscription.</span></span>

## <span data-ttu-id="c0430-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0430-104">SYNTAX</span></span>

```
New-AzsSubscription [-OfferId] <String> [[-DisplayName] <String>] [[-TenantId] <String>]
 [[-SubscriptionId] <String>] [[-State] <String>] [[-Location] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c0430-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c0430-105">DESCRIPTION</span></span>
<span data-ttu-id="c0430-106">Erstellen Sie ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c0430-106">Create a subscription.</span></span>

## <span data-ttu-id="c0430-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c0430-107">EXAMPLES</span></span>

### <span data-ttu-id="c0430-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c0430-108">EXAMPLE 1</span></span>
```
New-AzsSubscription -OfferId /delegatedProviders/default/offers/offer1
```

<span data-ttu-id="c0430-109">Erstellen Sie ein Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c0430-109">Create a subscription.</span></span>

## <span data-ttu-id="c0430-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0430-110">PARAMETERS</span></span>

### <span data-ttu-id="c0430-111">-Angebots-Nr</span><span class="sxs-lookup"><span data-stu-id="c0430-111">-OfferId</span></span>
<span data-ttu-id="c0430-112">Der Bezeichner des Angebots unter dem Bereich eines Delegierten Anbieters.</span><span class="sxs-lookup"><span data-stu-id="c0430-112">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="c0430-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c0430-113">-DisplayName</span></span>
<span data-ttu-id="c0430-114">Name des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="c0430-114">Subscription name.</span></span>

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

### <span data-ttu-id="c0430-115">-Mandanten-Nr</span><span class="sxs-lookup"><span data-stu-id="c0430-115">-TenantId</span></span>
<span data-ttu-id="c0430-116">Verzeichnis Mandanten-ID.</span><span class="sxs-lookup"><span data-stu-id="c0430-116">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="c0430-117">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="c0430-117">-SubscriptionId</span></span>
<span data-ttu-id="c0430-118">Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="c0430-118">Subscription identifier.</span></span>

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

### <span data-ttu-id="c0430-119">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="c0430-119">-State</span></span>
<span data-ttu-id="c0430-120">Status des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="c0430-120">Subscription state.</span></span>

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

### <span data-ttu-id="c0430-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="c0430-121">-Location</span></span>
<span data-ttu-id="c0430-122">Ort, an dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="c0430-122">Location where resource is location.</span></span>

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

### <span data-ttu-id="c0430-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0430-123">-WhatIf</span></span>
<span data-ttu-id="c0430-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c0430-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0430-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c0430-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0430-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c0430-126">-Confirm</span></span>
<span data-ttu-id="c0430-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c0430-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0430-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0430-128">CommonParameters</span></span>
<span data-ttu-id="c0430-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0430-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0430-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0430-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0430-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c0430-131">INPUTS</span></span>

## <span data-ttu-id="c0430-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c0430-132">OUTPUTS</span></span>

### <span data-ttu-id="c0430-133">Microsoft. AzureStack. Management. Subscription. Models. SubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="c0430-133">Microsoft.AzureStack.Management.Subscription.Models.SubscriptionModel</span></span>

## <span data-ttu-id="c0430-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="c0430-134">NOTES</span></span>

## <span data-ttu-id="c0430-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c0430-135">RELATED LINKS</span></span>
