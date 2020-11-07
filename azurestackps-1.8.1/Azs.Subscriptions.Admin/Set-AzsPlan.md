---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9ff6532cb43d7ece7460651eb4493201de4734b1
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93828060"
---
# <span data-ttu-id="9847b-101">Set-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="9847b-101">Set-AzsPlan</span></span>

## <span data-ttu-id="9847b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9847b-102">SYNOPSIS</span></span>
<span data-ttu-id="9847b-103">Aktualisiert den angegebenen Plan</span><span class="sxs-lookup"><span data-stu-id="9847b-103">Updates the specified plan</span></span>

## <span data-ttu-id="9847b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9847b-104">SYNTAX</span></span>

### <span data-ttu-id="9847b-105">Update (Standard)</span><span class="sxs-lookup"><span data-stu-id="9847b-105">Update (Default)</span></span>
```
Set-AzsPlan -Name <String> -ResourceGroupName <String> [-DisplayName <String>] [-QuotaIds <String[]>]
 [-SkuIds <String[]>] [-ExternalReferenceId <String>] [-Description <String>] [-Location <String>]
 [-SubscriptionCount <Int64>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9847b-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="9847b-106">InputObject</span></span>
```
Set-AzsPlan [-ResourceGroupName <String>] -InputObject <Plan> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9847b-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9847b-107">ResourceId</span></span>
```
Set-AzsPlan -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9847b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9847b-108">DESCRIPTION</span></span>
<span data-ttu-id="9847b-109">Aktualisiert den angegebenen Plan</span><span class="sxs-lookup"><span data-stu-id="9847b-109">Updates the specified plan</span></span>

## <span data-ttu-id="9847b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9847b-110">EXAMPLES</span></span>

### <span data-ttu-id="9847b-111">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="9847b-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsPlan -Name "plan1" -ResourceGroupName "rg1" -Description "This plan is meant to be used by accounting only."
```

<span data-ttu-id="9847b-112">Aktualisiert den angegebenen Plan</span><span class="sxs-lookup"><span data-stu-id="9847b-112">Updates the specified plan</span></span>

## <span data-ttu-id="9847b-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="9847b-113">PARAMETERS</span></span>

### <span data-ttu-id="9847b-114">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9847b-114">-Description</span></span>
<span data-ttu-id="9847b-115">Beschreibung des Plans</span><span class="sxs-lookup"><span data-stu-id="9847b-115">Description of the plan.</span></span>

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

### <span data-ttu-id="9847b-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9847b-116">-DisplayName</span></span>
<span data-ttu-id="9847b-117">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="9847b-117">Display name.</span></span>

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

### <span data-ttu-id="9847b-118">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="9847b-118">-ExternalReferenceId</span></span>
<span data-ttu-id="9847b-119">Externer Verweisbezeichner.</span><span class="sxs-lookup"><span data-stu-id="9847b-119">External reference identifier.</span></span>

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

### <span data-ttu-id="9847b-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9847b-120">-InputObject</span></span>
<span data-ttu-id="9847b-121">Das Eingabeobjekt vom Typ Microsoft. AzureStack. Management. Subscriptions. admin. Models. Plan.</span><span class="sxs-lookup"><span data-stu-id="9847b-121">The input object of type Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan.</span></span>

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

### <span data-ttu-id="9847b-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="9847b-122">-Location</span></span>
<span data-ttu-id="9847b-123">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="9847b-123">Location of the resource.</span></span>

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

### <span data-ttu-id="9847b-124">-Name</span><span class="sxs-lookup"><span data-stu-id="9847b-124">-Name</span></span>
<span data-ttu-id="9847b-125">Der Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="9847b-125">Name of the plan.</span></span>

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

### <span data-ttu-id="9847b-126">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="9847b-126">-QuotaIds</span></span>
<span data-ttu-id="9847b-127">Kontingent Bezeichner im Plan.</span><span class="sxs-lookup"><span data-stu-id="9847b-127">Quota identifiers under the plan.</span></span>

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

### <span data-ttu-id="9847b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9847b-128">-ResourceGroupName</span></span>
<span data-ttu-id="9847b-129">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="9847b-129">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="9847b-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="9847b-130">-ResourceId</span></span>
<span data-ttu-id="9847b-131">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="9847b-131">The resource id.</span></span>

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

### <span data-ttu-id="9847b-132">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="9847b-132">-SkuIds</span></span>
<span data-ttu-id="9847b-133">SKU-IDs.</span><span class="sxs-lookup"><span data-stu-id="9847b-133">SKU identifiers.</span></span>

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

### <span data-ttu-id="9847b-134">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="9847b-134">-SubscriptionCount</span></span>
<span data-ttu-id="9847b-135">Anzahl der Abonnements</span><span class="sxs-lookup"><span data-stu-id="9847b-135">Subscription count.</span></span>

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

### <span data-ttu-id="9847b-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9847b-136">-Confirm</span></span>
<span data-ttu-id="9847b-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9847b-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9847b-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9847b-138">-WhatIf</span></span>
<span data-ttu-id="9847b-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9847b-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9847b-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9847b-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9847b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9847b-141">CommonParameters</span></span>
<span data-ttu-id="9847b-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9847b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9847b-143">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9847b-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9847b-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9847b-144">INPUTS</span></span>

## <span data-ttu-id="9847b-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9847b-145">OUTPUTS</span></span>

### <span data-ttu-id="9847b-146">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Plan</span><span class="sxs-lookup"><span data-stu-id="9847b-146">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="9847b-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="9847b-147">NOTES</span></span>

## <span data-ttu-id="9847b-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9847b-148">RELATED LINKS</span></span>

