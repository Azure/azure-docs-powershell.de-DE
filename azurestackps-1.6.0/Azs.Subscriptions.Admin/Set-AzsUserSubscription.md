---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 106293e9d959aefe25ae3e4b27519639a39193d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475093"
---
# <span data-ttu-id="2d6cb-101">Set-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="2d6cb-101">Set-AzsUserSubscription</span></span>

## <span data-ttu-id="2d6cb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2d6cb-102">SYNOPSIS</span></span>
<span data-ttu-id="2d6cb-103">Aktualisieren des angegebenen Benutzer Abonnements</span><span class="sxs-lookup"><span data-stu-id="2d6cb-103">Updates the specified user subscription</span></span>

## <span data-ttu-id="2d6cb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d6cb-104">SYNTAX</span></span>

### <span data-ttu-id="2d6cb-105">Festlegen (Standard)</span><span class="sxs-lookup"><span data-stu-id="2d6cb-105">Set (Default)</span></span>
```
Set-AzsUserSubscription -SubscriptionId <Guid> [-DisplayName <String>]
 [-DelegatedProviderSubscriptionId <String>] [-Owner <String>] [-TenantId <String>]
 [-RoutingResourceManagerType <String>] [-ExternalReferenceId <String>] [-State <String>] [-Location <String>]
 [-OfferId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d6cb-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d6cb-106">ResourceId</span></span>
```
Set-AzsUserSubscription -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d6cb-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="2d6cb-107">InputObject</span></span>
```
Set-AzsUserSubscription -InputObject <Subscription> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d6cb-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2d6cb-108">DESCRIPTION</span></span>
<span data-ttu-id="2d6cb-109">Aktualisieren des angegebenen Benutzer Abonnements</span><span class="sxs-lookup"><span data-stu-id="2d6cb-109">Updates the specified user subscription</span></span>

## <span data-ttu-id="2d6cb-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2d6cb-110">EXAMPLES</span></span>

### <span data-ttu-id="2d6cb-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2d6cb-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsUserSubscription -SubscriptionId 8e425478-c7f0-49ca-bb92-b42889ec3642 -DisplayName "NewName"
```

<span data-ttu-id="2d6cb-112">Aktualisiert ein Abonnement</span><span class="sxs-lookup"><span data-stu-id="2d6cb-112">Updates a subscription</span></span>

## <span data-ttu-id="2d6cb-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d6cb-113">PARAMETERS</span></span>

### <span data-ttu-id="2d6cb-114">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2d6cb-114">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="2d6cb-115">ID des übergeordneten DelegatedProvider-Abonnements.</span><span class="sxs-lookup"><span data-stu-id="2d6cb-115">Parent DelegatedProvider subscription identifier.</span></span>

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

### <span data-ttu-id="2d6cb-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2d6cb-116">-DisplayName</span></span>
<span data-ttu-id="2d6cb-117">Name des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="2d6cb-117">Subscription name.</span></span>

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

### <span data-ttu-id="2d6cb-118">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="2d6cb-118">-ExternalReferenceId</span></span>
<span data-ttu-id="2d6cb-119">Externer Verweisbezeichner.</span><span class="sxs-lookup"><span data-stu-id="2d6cb-119">External reference identifier.</span></span>

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

### <span data-ttu-id="2d6cb-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2d6cb-120">-InputObject</span></span>
<span data-ttu-id="2d6cb-121">Das Eingabeobjekt vom Typ Microsoft. AzureStack. Management. Network. admin. Models. Quota.</span><span class="sxs-lookup"><span data-stu-id="2d6cb-121">The input object of type Microsoft.AzureStack.Management.Network.Admin.Models.Quota.</span></span>

```yaml
Type: Subscription
Parameter Sets: InputObject
Aliases: Subscription

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2d6cb-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="2d6cb-122">-Location</span></span>
<span data-ttu-id="2d6cb-123">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="2d6cb-123">Location of the resource.</span></span>

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

### <span data-ttu-id="2d6cb-124">-Angebots-Nr</span><span class="sxs-lookup"><span data-stu-id="2d6cb-124">-OfferId</span></span>
<span data-ttu-id="2d6cb-125">Der Bezeichner des Angebots unter dem Bereich eines Delegierten Anbieters.</span><span class="sxs-lookup"><span data-stu-id="2d6cb-125">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="2d6cb-126">-Besitzer</span><span class="sxs-lookup"><span data-stu-id="2d6cb-126">-Owner</span></span>
<span data-ttu-id="2d6cb-127">Besitzer des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="2d6cb-127">Subscription owner.</span></span>

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

### <span data-ttu-id="2d6cb-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2d6cb-128">-ResourceId</span></span>
<span data-ttu-id="2d6cb-129">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="2d6cb-129">The resource ID.</span></span>

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

### <span data-ttu-id="2d6cb-130">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="2d6cb-130">-RoutingResourceManagerType</span></span>
<span data-ttu-id="2d6cb-131">Typ des Routing Ressourcen-Managers.</span><span class="sxs-lookup"><span data-stu-id="2d6cb-131">Routing resource manager type.</span></span>

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

### <span data-ttu-id="2d6cb-132">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="2d6cb-132">-State</span></span>
<span data-ttu-id="2d6cb-133">Status des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="2d6cb-133">Subscription state.</span></span>

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

### <span data-ttu-id="2d6cb-134">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="2d6cb-134">-SubscriptionId</span></span>
<span data-ttu-id="2d6cb-135">Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="2d6cb-135">Subscription identifier.</span></span>

```yaml
Type: Guid
Parameter Sets: Set
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d6cb-136">-Mandanten-Nr</span><span class="sxs-lookup"><span data-stu-id="2d6cb-136">-TenantId</span></span>
<span data-ttu-id="2d6cb-137">Verzeichnis Mandanten-ID.</span><span class="sxs-lookup"><span data-stu-id="2d6cb-137">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="2d6cb-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2d6cb-138">-Confirm</span></span>
<span data-ttu-id="2d6cb-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2d6cb-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d6cb-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d6cb-140">-WhatIf</span></span>
<span data-ttu-id="2d6cb-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2d6cb-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d6cb-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2d6cb-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d6cb-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d6cb-143">CommonParameters</span></span>
<span data-ttu-id="2d6cb-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d6cb-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d6cb-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d6cb-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d6cb-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2d6cb-146">INPUTS</span></span>

## <span data-ttu-id="2d6cb-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2d6cb-147">OUTPUTS</span></span>

### <span data-ttu-id="2d6cb-148">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Subscription</span><span class="sxs-lookup"><span data-stu-id="2d6cb-148">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="2d6cb-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="2d6cb-149">NOTES</span></span>

## <span data-ttu-id="2d6cb-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2d6cb-150">RELATED LINKS</span></span>

