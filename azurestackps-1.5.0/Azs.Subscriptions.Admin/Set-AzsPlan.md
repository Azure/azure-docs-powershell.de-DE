---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0f03365a81fc53af14e3fc9e686504ef3e4387c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475237"
---
# <span data-ttu-id="8e32a-101">Set-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="8e32a-101">Set-AzsPlan</span></span>

## <span data-ttu-id="8e32a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8e32a-102">SYNOPSIS</span></span>
<span data-ttu-id="8e32a-103">Aktualisiert den angegebenen Plan</span><span class="sxs-lookup"><span data-stu-id="8e32a-103">Updates the specified plan</span></span>

## <span data-ttu-id="8e32a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e32a-104">SYNTAX</span></span>

### <span data-ttu-id="8e32a-105">Update (Standard)</span><span class="sxs-lookup"><span data-stu-id="8e32a-105">Update (Default)</span></span>
```
Set-AzsPlan -Name <String> -ResourceGroupName <String> [-DisplayName <String>] [-QuotaIds <String[]>]
 [-SkuIds <String[]>] [-ExternalReferenceId <String>] [-Description <String>] [-Location <String>]
 [-SubscriptionCount <Int64>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e32a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="8e32a-106">InputObject</span></span>
```
Set-AzsPlan [-ResourceGroupName <String>] -InputObject <Plan> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e32a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e32a-107">ResourceId</span></span>
```
Set-AzsPlan -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e32a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8e32a-108">DESCRIPTION</span></span>
<span data-ttu-id="8e32a-109">Aktualisiert den angegebenen Plan</span><span class="sxs-lookup"><span data-stu-id="8e32a-109">Updates the specified plan</span></span>

## <span data-ttu-id="8e32a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8e32a-110">EXAMPLES</span></span>

### <span data-ttu-id="8e32a-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8e32a-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsPlan -Name "plan1" -ResourceGroupName "rg1" -Description "This plan is meant to be used by accounting only."
```

<span data-ttu-id="8e32a-112">Aktualisiert den angegebenen Plan</span><span class="sxs-lookup"><span data-stu-id="8e32a-112">Updates the specified plan</span></span>

## <span data-ttu-id="8e32a-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e32a-113">PARAMETERS</span></span>

### <span data-ttu-id="8e32a-114">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8e32a-114">-Description</span></span>
<span data-ttu-id="8e32a-115">Beschreibung des Plans</span><span class="sxs-lookup"><span data-stu-id="8e32a-115">Description of the plan.</span></span>

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

### <span data-ttu-id="8e32a-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8e32a-116">-DisplayName</span></span>
<span data-ttu-id="8e32a-117">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="8e32a-117">Display name.</span></span>

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

### <span data-ttu-id="8e32a-118">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="8e32a-118">-ExternalReferenceId</span></span>
<span data-ttu-id="8e32a-119">Externer Verweisbezeichner.</span><span class="sxs-lookup"><span data-stu-id="8e32a-119">External reference identifier.</span></span>

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

### <span data-ttu-id="8e32a-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8e32a-120">-InputObject</span></span>
<span data-ttu-id="8e32a-121">Das Eingabeobjekt vom Typ Microsoft. AzureStack. Management. Subscriptions. admin. Models. Plan.</span><span class="sxs-lookup"><span data-stu-id="8e32a-121">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan.</span></span>

```yaml
Type: Plan
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e32a-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="8e32a-122">-Location</span></span>
<span data-ttu-id="8e32a-123">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="8e32a-123">Location of the resource.</span></span>

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

### <span data-ttu-id="8e32a-124">-Name</span><span class="sxs-lookup"><span data-stu-id="8e32a-124">-Name</span></span>
<span data-ttu-id="8e32a-125">Der Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="8e32a-125">Name of the plan.</span></span>

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

### <span data-ttu-id="8e32a-126">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="8e32a-126">-QuotaIds</span></span>
<span data-ttu-id="8e32a-127">Kontingent Bezeichner im Plan.</span><span class="sxs-lookup"><span data-stu-id="8e32a-127">Quota identifiers under the plan.</span></span>

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

### <span data-ttu-id="8e32a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e32a-128">-ResourceGroupName</span></span>
<span data-ttu-id="8e32a-129">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="8e32a-129">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="8e32a-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="8e32a-130">-ResourceId</span></span>
<span data-ttu-id="8e32a-131">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="8e32a-131">The resource id.</span></span>

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

### <span data-ttu-id="8e32a-132">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="8e32a-132">-SkuIds</span></span>
<span data-ttu-id="8e32a-133">SKU-IDs.</span><span class="sxs-lookup"><span data-stu-id="8e32a-133">SKU identifiers.</span></span>

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

### <span data-ttu-id="8e32a-134">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="8e32a-134">-SubscriptionCount</span></span>
<span data-ttu-id="8e32a-135">Anzahl der Abonnements</span><span class="sxs-lookup"><span data-stu-id="8e32a-135">Subscription count.</span></span>

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

### <span data-ttu-id="8e32a-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8e32a-136">-Confirm</span></span>
<span data-ttu-id="8e32a-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8e32a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e32a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e32a-138">-WhatIf</span></span>
<span data-ttu-id="8e32a-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8e32a-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e32a-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8e32a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e32a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e32a-141">CommonParameters</span></span>
<span data-ttu-id="8e32a-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e32a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e32a-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e32a-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e32a-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8e32a-144">INPUTS</span></span>

## <span data-ttu-id="8e32a-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8e32a-145">OUTPUTS</span></span>

### <span data-ttu-id="8e32a-146">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Plan</span><span class="sxs-lookup"><span data-stu-id="8e32a-146">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="8e32a-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="8e32a-147">NOTES</span></span>

## <span data-ttu-id="8e32a-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8e32a-148">RELATED LINKS</span></span>

