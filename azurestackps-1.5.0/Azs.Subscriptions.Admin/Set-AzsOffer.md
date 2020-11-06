---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 285b9509241e9035c007f871ac6395008a1f9cde
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475597"
---
# <span data-ttu-id="f3c3f-101">Set-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="f3c3f-101">Set-AzsOffer</span></span>

## <span data-ttu-id="f3c3f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f3c3f-102">SYNOPSIS</span></span>
<span data-ttu-id="f3c3f-103">Aktualisieren Sie das Angebot.</span><span class="sxs-lookup"><span data-stu-id="f3c3f-103">Update the offer.</span></span>

## <span data-ttu-id="f3c3f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3c3f-104">SYNTAX</span></span>

### <span data-ttu-id="f3c3f-105">Update (Standard)</span><span class="sxs-lookup"><span data-stu-id="f3c3f-105">Update (Default)</span></span>
```
Set-AzsOffer -Name <String> -ResourceGroupName <String> [-DisplayName <String>] [-BasePlanIds <String[]>]
 [-Description <String>] [-ExternalReferenceId <String>] [-State <String>] [-Location <String>]
 [-SubscriptionCount <Int64>] [-MaxSubscriptionsPerAccount <Int64>]
 [-AddonPlanDefinition <AddonPlanDefinition[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3c3f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f3c3f-106">InputObject</span></span>
```
Set-AzsOffer [-ResourceGroupName <String>] -InputObject <Offer> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3c3f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3c3f-107">ResourceId</span></span>
```
Set-AzsOffer -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3c3f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3c3f-108">DESCRIPTION</span></span>
<span data-ttu-id="f3c3f-109">Aktualisieren Sie das Angebot.</span><span class="sxs-lookup"><span data-stu-id="f3c3f-109">Update the offer.</span></span>

## <span data-ttu-id="f3c3f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f3c3f-110">EXAMPLES</span></span>

### <span data-ttu-id="f3c3f-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f3c3f-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsOffer -Name offer1 -ResourceGroupName rg1 -State Private
```

<span data-ttu-id="f3c3f-112">Aktualisieren Sie das Angebot.</span><span class="sxs-lookup"><span data-stu-id="f3c3f-112">Update the offer.</span></span>

## <span data-ttu-id="f3c3f-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3c3f-113">PARAMETERS</span></span>

### <span data-ttu-id="f3c3f-114">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="f3c3f-114">-AddonPlanDefinition</span></span>
<span data-ttu-id="f3c3f-115">Verweise auf Add-on-Pläne, die ein Mandant optional als Teil des Angebots erwerben kann.</span><span class="sxs-lookup"><span data-stu-id="f3c3f-115">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>

```yaml
Type: AddonPlanDefinition[]
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c3f-116">-BasePlanIds</span><span class="sxs-lookup"><span data-stu-id="f3c3f-116">-BasePlanIds</span></span>
<span data-ttu-id="f3c3f-117">Bezeichner der Basispläne, die dem Mandanten sofort zur Verfügung gestellt werden, wenn ein Mandant das Angebot abonniert hat.</span><span class="sxs-lookup"><span data-stu-id="f3c3f-117">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

```yaml
Type: String[]
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c3f-118">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3c3f-118">-Description</span></span>
<span data-ttu-id="f3c3f-119">Angebotsbeschreibung.</span><span class="sxs-lookup"><span data-stu-id="f3c3f-119">Description of offer.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c3f-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f3c3f-120">-DisplayName</span></span>
<span data-ttu-id="f3c3f-121">Anzeigename des Angebots.</span><span class="sxs-lookup"><span data-stu-id="f3c3f-121">Display name of offer.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c3f-122">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="f3c3f-122">-ExternalReferenceId</span></span>
<span data-ttu-id="f3c3f-123">Externer Verweisbezeichner.</span><span class="sxs-lookup"><span data-stu-id="f3c3f-123">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c3f-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f3c3f-124">-InputObject</span></span>
<span data-ttu-id="f3c3f-125">Das Eingabeobjekt vom Typ Microsoft. AzureStack. Management. Subscriptions. admin. Models. offer.</span><span class="sxs-lookup"><span data-stu-id="f3c3f-125">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer.</span></span>

```yaml
Type: Offer
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3c3f-126">-Standort</span><span class="sxs-lookup"><span data-stu-id="f3c3f-126">-Location</span></span>
<span data-ttu-id="f3c3f-127">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="f3c3f-127">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c3f-128">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="f3c3f-128">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="f3c3f-129">Maximale Abonnements pro Konto.</span><span class="sxs-lookup"><span data-stu-id="f3c3f-129">Maximum subscriptions per account.</span></span>

```yaml
Type: Int64
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c3f-130">-Name</span><span class="sxs-lookup"><span data-stu-id="f3c3f-130">-Name</span></span>
<span data-ttu-id="f3c3f-131">Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="f3c3f-131">Name of an offer.</span></span>

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

### <span data-ttu-id="f3c3f-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3c3f-132">-ResourceGroupName</span></span>
<span data-ttu-id="f3c3f-133">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="f3c3f-133">The resource group the resource is located under.</span></span>

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

```yaml
Type: String
Parameter Sets: InputObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c3f-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f3c3f-134">-ResourceId</span></span>
<span data-ttu-id="f3c3f-135">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="f3c3f-135">The resource id.</span></span>

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

### <span data-ttu-id="f3c3f-136">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="f3c3f-136">-State</span></span>
<span data-ttu-id="f3c3f-137">Barrierefreien Status anbieten.</span><span class="sxs-lookup"><span data-stu-id="f3c3f-137">Offer accessibility state.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c3f-138">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="f3c3f-138">-SubscriptionCount</span></span>
<span data-ttu-id="f3c3f-139">Aktuelle Abonnementanzahl.</span><span class="sxs-lookup"><span data-stu-id="f3c3f-139">Current subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3c3f-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f3c3f-140">-Confirm</span></span>
<span data-ttu-id="f3c3f-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f3c3f-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3c3f-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3c3f-142">-WhatIf</span></span>
<span data-ttu-id="f3c3f-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f3c3f-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3c3f-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f3c3f-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3c3f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3c3f-145">CommonParameters</span></span>
<span data-ttu-id="f3c3f-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3c3f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3c3f-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3c3f-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3c3f-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f3c3f-148">INPUTS</span></span>

## <span data-ttu-id="f3c3f-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f3c3f-149">OUTPUTS</span></span>

### <span data-ttu-id="f3c3f-150">Microsoft. AzureStack. Management. Subscriptions. admin. Models. offer</span><span class="sxs-lookup"><span data-stu-id="f3c3f-150">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="f3c3f-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="f3c3f-151">NOTES</span></span>

## <span data-ttu-id="f3c3f-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f3c3f-152">RELATED LINKS</span></span>

