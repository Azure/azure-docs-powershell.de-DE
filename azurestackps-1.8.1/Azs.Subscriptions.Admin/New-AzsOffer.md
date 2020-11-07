---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cce59bbbef69f10f39478d784d688a4f1de312fb
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93828179"
---
# <span data-ttu-id="2d24e-101">New-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="2d24e-101">New-AzsOffer</span></span>

## <span data-ttu-id="2d24e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2d24e-102">SYNOPSIS</span></span>
<span data-ttu-id="2d24e-103">Erstellt ein neues Angebot.</span><span class="sxs-lookup"><span data-stu-id="2d24e-103">Creates a new offer.</span></span>

## <span data-ttu-id="2d24e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d24e-104">SYNTAX</span></span>

```
New-AzsOffer [-Name] <String> [-DisplayName] <String> [-ResourceGroupName] <String> [[-BasePlanIds] <String[]>]
 [[-Description] <String>] [[-ExternalReferenceId] <String>] [[-State] <String>] [[-Location] <String>]
 [[-MaxSubscriptionsPerAccount] <Int64>] [[-SubscriptionCount] <Int64>]
 [[-AddonPlanDefinition] <AddonPlanDefinition[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d24e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2d24e-105">DESCRIPTION</span></span>
<span data-ttu-id="2d24e-106">Erstellen oder aktualisieren Sie das Angebot.</span><span class="sxs-lookup"><span data-stu-id="2d24e-106">Create or update the offer.</span></span>

## <span data-ttu-id="2d24e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2d24e-107">EXAMPLES</span></span>

### <span data-ttu-id="2d24e-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2d24e-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsOffer -Name offer1 -ResourceGroupName rg1 -State Public -DisplayName "offer1" -BasePlanIds "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/resourceGroups/rg1/providers/Microsoft.Subscriptions.Admin/plans/plan1"
```

<span data-ttu-id="2d24e-109">Erstellt ein neues Angebot.</span><span class="sxs-lookup"><span data-stu-id="2d24e-109">Creates a new offer.</span></span>

## <span data-ttu-id="2d24e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d24e-110">PARAMETERS</span></span>

### <span data-ttu-id="2d24e-111">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="2d24e-111">-AddonPlanDefinition</span></span>
<span data-ttu-id="2d24e-112">Verweise auf Add-on-Pläne, die ein Mandant optional als Teil des Angebots erwerben kann.</span><span class="sxs-lookup"><span data-stu-id="2d24e-112">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>

```yaml
Type: AddonPlanDefinition[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d24e-113">-BasePlanIds</span><span class="sxs-lookup"><span data-stu-id="2d24e-113">-BasePlanIds</span></span>
<span data-ttu-id="2d24e-114">Bezeichner der Basispläne, die dem Mandanten sofort zur Verfügung gestellt werden, wenn ein Mandant das Angebot abonniert hat.</span><span class="sxs-lookup"><span data-stu-id="2d24e-114">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d24e-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2d24e-115">-Description</span></span>
<span data-ttu-id="2d24e-116">Angebotsbeschreibung.</span><span class="sxs-lookup"><span data-stu-id="2d24e-116">Description of offer.</span></span>

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

### <span data-ttu-id="2d24e-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2d24e-117">-DisplayName</span></span>
<span data-ttu-id="2d24e-118">Anzeigename des Angebots.</span><span class="sxs-lookup"><span data-stu-id="2d24e-118">Display name of offer.</span></span>

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

### <span data-ttu-id="2d24e-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="2d24e-119">-ExternalReferenceId</span></span>
<span data-ttu-id="2d24e-120">Externer Verweisbezeichner.</span><span class="sxs-lookup"><span data-stu-id="2d24e-120">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d24e-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="2d24e-121">-Location</span></span>
<span data-ttu-id="2d24e-122">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="2d24e-122">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ArmLocation

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d24e-123">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="2d24e-123">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="2d24e-124">Maximale Abonnements pro Konto.</span><span class="sxs-lookup"><span data-stu-id="2d24e-124">Maximum subscriptions per account.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d24e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="2d24e-125">-Name</span></span>
<span data-ttu-id="2d24e-126">Name eines Angebots.</span><span class="sxs-lookup"><span data-stu-id="2d24e-126">Name of an offer.</span></span>

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

### <span data-ttu-id="2d24e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d24e-127">-ResourceGroupName</span></span>
<span data-ttu-id="2d24e-128">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="2d24e-128">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d24e-129">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="2d24e-129">-State</span></span>
<span data-ttu-id="2d24e-130">Barrierefreien Status anbieten.</span><span class="sxs-lookup"><span data-stu-id="2d24e-130">Offer accessibility state.</span></span>
<span data-ttu-id="2d24e-131">Der Standardwert ist "Privat".</span><span class="sxs-lookup"><span data-stu-id="2d24e-131">Default value is Private.</span></span>
<span data-ttu-id="2d24e-132">Dieser Parameter wird in einer zukünftigen Version als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="2d24e-132">This parameter will be deprecated in a future release</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: Private
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d24e-133">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="2d24e-133">-SubscriptionCount</span></span>
<span data-ttu-id="2d24e-134">Aktuelle Abonnementanzahl.</span><span class="sxs-lookup"><span data-stu-id="2d24e-134">Current subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d24e-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2d24e-135">-Confirm</span></span>
<span data-ttu-id="2d24e-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2d24e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d24e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d24e-137">-WhatIf</span></span>
<span data-ttu-id="2d24e-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2d24e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d24e-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2d24e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d24e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d24e-140">CommonParameters</span></span>
<span data-ttu-id="2d24e-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d24e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d24e-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d24e-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d24e-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2d24e-143">INPUTS</span></span>

## <span data-ttu-id="2d24e-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2d24e-144">OUTPUTS</span></span>

### <span data-ttu-id="2d24e-145">Microsoft. AzureStack. Management. Subscriptions. admin. Models. offer</span><span class="sxs-lookup"><span data-stu-id="2d24e-145">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="2d24e-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="2d24e-146">NOTES</span></span>

## <span data-ttu-id="2d24e-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2d24e-147">RELATED LINKS</span></span>

