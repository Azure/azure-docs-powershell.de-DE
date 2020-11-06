---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 33544da0c95e6b53da2a0dc189ca0dfe538da270
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93474750"
---
# <span data-ttu-id="c76b4-101">New-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="c76b4-101">New-AzsUserSubscription</span></span>

## <span data-ttu-id="c76b4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c76b4-102">SYNOPSIS</span></span>
<span data-ttu-id="c76b4-103">Erstellen Sie ein neues Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c76b4-103">Create a new subscription.</span></span>

## <span data-ttu-id="c76b4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c76b4-104">SYNTAX</span></span>

```
New-AzsUserSubscription [-Owner] <String> [-OfferId] <String> [[-TenantId] <String>] [[-DisplayName] <String>]
 [[-DelegatedProviderSubscriptionId] <String>] [[-RoutingResourceManagerType] <String>]
 [[-ExternalReferenceId] <String>] [[-State] <String>] [[-SubscriptionId] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c76b4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c76b4-105">DESCRIPTION</span></span>
<span data-ttu-id="c76b4-106">Erstellen Sie ein neues Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c76b4-106">Create a new subscription.</span></span>

## <span data-ttu-id="c76b4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c76b4-107">EXAMPLES</span></span>

### <span data-ttu-id="c76b4-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c76b4-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsUserSubscription -Owner user@contoso.com -OfferId "/subscriptions/302d0fcd-5263-4f4d-82ba-383ad95a3e53/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/offers/offer1"
```

<span data-ttu-id="c76b4-109">Erstellt ein neues Benutzer Abonnement</span><span class="sxs-lookup"><span data-stu-id="c76b4-109">Creates a new user subscription</span></span>

## <span data-ttu-id="c76b4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c76b4-110">PARAMETERS</span></span>

### <span data-ttu-id="c76b4-111">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c76b4-111">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="c76b4-112">ID des übergeordneten DelegatedProvider-Abonnements.</span><span class="sxs-lookup"><span data-stu-id="c76b4-112">Parent DelegatedProvider subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c76b4-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c76b4-113">-DisplayName</span></span>
<span data-ttu-id="c76b4-114">Name des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="c76b4-114">Subscription name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c76b4-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="c76b4-115">-ExternalReferenceId</span></span>
<span data-ttu-id="c76b4-116">Externer Verweisbezeichner.</span><span class="sxs-lookup"><span data-stu-id="c76b4-116">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c76b4-117">-Angebots-Nr</span><span class="sxs-lookup"><span data-stu-id="c76b4-117">-OfferId</span></span>
<span data-ttu-id="c76b4-118">Der Bezeichner des Angebots unter dem Bereich eines Delegierten Anbieters.</span><span class="sxs-lookup"><span data-stu-id="c76b4-118">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c76b4-119">-Besitzer</span><span class="sxs-lookup"><span data-stu-id="c76b4-119">-Owner</span></span>
<span data-ttu-id="c76b4-120">Besitzer des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="c76b4-120">Subscription owner.</span></span>

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

### <span data-ttu-id="c76b4-121">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="c76b4-121">-RoutingResourceManagerType</span></span>
<span data-ttu-id="c76b4-122">Typ des Routing Ressourcen-Managers.</span><span class="sxs-lookup"><span data-stu-id="c76b4-122">Routing resource manager type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: Default
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c76b4-123">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="c76b4-123">-State</span></span>
<span data-ttu-id="c76b4-124">Status des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="c76b4-124">Subscription state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: Enabled
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c76b4-125">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="c76b4-125">-SubscriptionId</span></span>
<span data-ttu-id="c76b4-126">Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="c76b4-126">Subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c76b4-127">-Mandanten-Nr</span><span class="sxs-lookup"><span data-stu-id="c76b4-127">-TenantId</span></span>
<span data-ttu-id="c76b4-128">Verzeichnis Mandanten-ID.</span><span class="sxs-lookup"><span data-stu-id="c76b4-128">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="c76b4-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c76b4-129">-Confirm</span></span>
<span data-ttu-id="c76b4-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c76b4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c76b4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c76b4-131">-WhatIf</span></span>
<span data-ttu-id="c76b4-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c76b4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c76b4-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c76b4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c76b4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c76b4-134">CommonParameters</span></span>
<span data-ttu-id="c76b4-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c76b4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c76b4-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c76b4-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c76b4-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c76b4-137">INPUTS</span></span>

## <span data-ttu-id="c76b4-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c76b4-138">OUTPUTS</span></span>

### <span data-ttu-id="c76b4-139">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Subscription</span><span class="sxs-lookup"><span data-stu-id="c76b4-139">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="c76b4-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="c76b4-140">NOTES</span></span>

## <span data-ttu-id="c76b4-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c76b4-141">RELATED LINKS</span></span>

