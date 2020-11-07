---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 348f7dc1f4719e70a73902b59cf335bb22015bec
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2020
ms.locfileid: "93827511"
---
# <span data-ttu-id="c6027-101">New-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="c6027-101">New-AzsPlan</span></span>

## <span data-ttu-id="c6027-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c6027-102">SYNOPSIS</span></span>
<span data-ttu-id="c6027-103">Erstellt einen neuen Plan</span><span class="sxs-lookup"><span data-stu-id="c6027-103">Creates a new plan</span></span>

## <span data-ttu-id="c6027-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6027-104">SYNTAX</span></span>

```
New-AzsPlan [-Name] <String> [-ResourceGroupName] <String> [-DisplayName] <String> [-QuotaIds] <String[]>
 [[-Description] <String>] [[-SkuIds] <String[]>] [[-ExternalReferenceId] <String>] [[-Location] <String>]
 [[-SubscriptionCount] <Int64>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6027-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c6027-105">DESCRIPTION</span></span>
<span data-ttu-id="c6027-106">Erstellt einen neuen Plan</span><span class="sxs-lookup"><span data-stu-id="c6027-106">Creates a new plan</span></span>

## <span data-ttu-id="c6027-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c6027-107">EXAMPLES</span></span>

### <span data-ttu-id="c6027-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c6027-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsPlan -Name "plan1" -ResourceGroupName "rg1" -QuotaIds "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/providers/Microsoft.Subscriptions.Admin/locations/local/quotas/delegatedProviderQuota" -Location "local" -DisplayName "plan1" -Description "asda"
```

<span data-ttu-id="c6027-109">Erstellt einen neuen Plan</span><span class="sxs-lookup"><span data-stu-id="c6027-109">Creates a new plan</span></span>

## <span data-ttu-id="c6027-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6027-110">PARAMETERS</span></span>

### <span data-ttu-id="c6027-111">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c6027-111">-Description</span></span>
<span data-ttu-id="c6027-112">Beschreibung des Plans</span><span class="sxs-lookup"><span data-stu-id="c6027-112">Description of the plan.</span></span>

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

### <span data-ttu-id="c6027-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c6027-113">-DisplayName</span></span>
<span data-ttu-id="c6027-114">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="c6027-114">Display name.</span></span>

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

### <span data-ttu-id="c6027-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="c6027-115">-ExternalReferenceId</span></span>
<span data-ttu-id="c6027-116">Externer Verweisbezeichner.</span><span class="sxs-lookup"><span data-stu-id="c6027-116">External reference identifier.</span></span>

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

### <span data-ttu-id="c6027-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="c6027-117">-Location</span></span>
<span data-ttu-id="c6027-118">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="c6027-118">Location of the resource.</span></span>

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

### <span data-ttu-id="c6027-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c6027-119">-Name</span></span>
<span data-ttu-id="c6027-120">Der Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="c6027-120">Name of the plan.</span></span>

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

### <span data-ttu-id="c6027-121">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="c6027-121">-QuotaIds</span></span>
<span data-ttu-id="c6027-122">Kontingent Bezeichner im Plan.</span><span class="sxs-lookup"><span data-stu-id="c6027-122">Quota identifiers under the plan.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6027-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6027-123">-ResourceGroupName</span></span>
<span data-ttu-id="c6027-124">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="c6027-124">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="c6027-125">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="c6027-125">-SkuIds</span></span>
<span data-ttu-id="c6027-126">SKU-IDs.</span><span class="sxs-lookup"><span data-stu-id="c6027-126">SKU identifiers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6027-127">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="c6027-127">-SubscriptionCount</span></span>
<span data-ttu-id="c6027-128">Anzahl der Abonnements</span><span class="sxs-lookup"><span data-stu-id="c6027-128">Subscription count.</span></span>

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

### <span data-ttu-id="c6027-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c6027-129">-Confirm</span></span>
<span data-ttu-id="c6027-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c6027-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6027-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6027-131">-WhatIf</span></span>
<span data-ttu-id="c6027-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c6027-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6027-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c6027-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6027-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6027-134">CommonParameters</span></span>
<span data-ttu-id="c6027-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6027-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6027-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6027-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6027-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c6027-137">INPUTS</span></span>

## <span data-ttu-id="c6027-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c6027-138">OUTPUTS</span></span>

### <span data-ttu-id="c6027-139">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Plan</span><span class="sxs-lookup"><span data-stu-id="c6027-139">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="c6027-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="c6027-140">NOTES</span></span>

## <span data-ttu-id="c6027-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c6027-141">RELATED LINKS</span></span>

