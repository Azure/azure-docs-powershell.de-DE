---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ef53ac2d32d71a68b7fe342f5d2d0cafc2a193f8
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93828103"
---
# <span data-ttu-id="42501-101">Set-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="42501-101">Set-AzsUserSubscription</span></span>

## <span data-ttu-id="42501-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="42501-102">SYNOPSIS</span></span>
<span data-ttu-id="42501-103">Aktualisieren des angegebenen Benutzer Abonnements</span><span class="sxs-lookup"><span data-stu-id="42501-103">Updates the specified user subscription</span></span>

## <span data-ttu-id="42501-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="42501-104">SYNTAX</span></span>

### <span data-ttu-id="42501-105">Festlegen (Standard)</span><span class="sxs-lookup"><span data-stu-id="42501-105">Set (Default)</span></span>
```
Set-AzsUserSubscription -SubscriptionId <Guid> [-DisplayName <String>]
 [-DelegatedProviderSubscriptionId <String>] [-Owner <String>] [-TenantId <String>]
 [-RoutingResourceManagerType <String>] [-ExternalReferenceId <String>] [-State <String>] [-Location <String>]
 [-OfferId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42501-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="42501-106">ResourceId</span></span>
```
Set-AzsUserSubscription -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42501-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="42501-107">InputObject</span></span>
```
Set-AzsUserSubscription -InputObject <Subscription> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42501-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42501-108">DESCRIPTION</span></span>
<span data-ttu-id="42501-109">Aktualisieren des angegebenen Benutzer Abonnements</span><span class="sxs-lookup"><span data-stu-id="42501-109">Updates the specified user subscription</span></span>

## <span data-ttu-id="42501-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="42501-110">EXAMPLES</span></span>

### <span data-ttu-id="42501-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="42501-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsUserSubscription -SubscriptionId 8e425478-c7f0-49ca-bb92-b42889ec3642 -DisplayName "NewName"
```

<span data-ttu-id="42501-112">Aktualisiert ein Abonnement</span><span class="sxs-lookup"><span data-stu-id="42501-112">Updates a subscription</span></span>

## <span data-ttu-id="42501-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="42501-113">PARAMETERS</span></span>

### <span data-ttu-id="42501-114">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="42501-114">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="42501-115">ID des übergeordneten DelegatedProvider-Abonnements.</span><span class="sxs-lookup"><span data-stu-id="42501-115">Parent DelegatedProvider subscription identifier.</span></span>

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

### <span data-ttu-id="42501-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="42501-116">-DisplayName</span></span>
<span data-ttu-id="42501-117">Name des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="42501-117">Subscription name.</span></span>

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

### <span data-ttu-id="42501-118">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="42501-118">-ExternalReferenceId</span></span>
<span data-ttu-id="42501-119">Externer Verweisbezeichner.</span><span class="sxs-lookup"><span data-stu-id="42501-119">External reference identifier.</span></span>

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

### <span data-ttu-id="42501-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="42501-120">-InputObject</span></span>
<span data-ttu-id="42501-121">Das Eingabeobjekt vom Typ Microsoft. AzureStack. Management. Network. admin. Models. Quota.</span><span class="sxs-lookup"><span data-stu-id="42501-121">The input object of type Microsoft.AzureStack.Management.Network.Admin.Models.Quota.</span></span>

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

### <span data-ttu-id="42501-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="42501-122">-Location</span></span>
<span data-ttu-id="42501-123">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="42501-123">Location of the resource.</span></span>

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

### <span data-ttu-id="42501-124">-Angebots-Nr</span><span class="sxs-lookup"><span data-stu-id="42501-124">-OfferId</span></span>
<span data-ttu-id="42501-125">Der Bezeichner des Angebots unter dem Bereich eines Delegierten Anbieters.</span><span class="sxs-lookup"><span data-stu-id="42501-125">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="42501-126">-Besitzer</span><span class="sxs-lookup"><span data-stu-id="42501-126">-Owner</span></span>
<span data-ttu-id="42501-127">Besitzer des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="42501-127">Subscription owner.</span></span>

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

### <span data-ttu-id="42501-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="42501-128">-ResourceId</span></span>
<span data-ttu-id="42501-129">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="42501-129">The resource ID.</span></span>

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

### <span data-ttu-id="42501-130">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="42501-130">-RoutingResourceManagerType</span></span>
<span data-ttu-id="42501-131">Typ des Routing Ressourcen-Managers.</span><span class="sxs-lookup"><span data-stu-id="42501-131">Routing resource manager type.</span></span>

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

### <span data-ttu-id="42501-132">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="42501-132">-State</span></span>
<span data-ttu-id="42501-133">Status des Abonnements.</span><span class="sxs-lookup"><span data-stu-id="42501-133">Subscription state.</span></span>

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

### <span data-ttu-id="42501-134">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="42501-134">-SubscriptionId</span></span>
<span data-ttu-id="42501-135">Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="42501-135">Subscription identifier.</span></span>

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

### <span data-ttu-id="42501-136">-Mandanten-Nr</span><span class="sxs-lookup"><span data-stu-id="42501-136">-TenantId</span></span>
<span data-ttu-id="42501-137">Verzeichnis Mandanten-ID.</span><span class="sxs-lookup"><span data-stu-id="42501-137">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="42501-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="42501-138">-Confirm</span></span>
<span data-ttu-id="42501-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="42501-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42501-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42501-140">-WhatIf</span></span>
<span data-ttu-id="42501-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="42501-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42501-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="42501-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42501-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42501-143">CommonParameters</span></span>
<span data-ttu-id="42501-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42501-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42501-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42501-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42501-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="42501-146">INPUTS</span></span>

## <span data-ttu-id="42501-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="42501-147">OUTPUTS</span></span>

### <span data-ttu-id="42501-148">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Subscription</span><span class="sxs-lookup"><span data-stu-id="42501-148">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="42501-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="42501-149">NOTES</span></span>

## <span data-ttu-id="42501-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="42501-150">RELATED LINKS</span></span>

