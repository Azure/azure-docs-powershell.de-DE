---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 348f7dc1f4719e70a73902b59cf335bb22015bec
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93840840"
---
# <span data-ttu-id="8027d-101">New-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="8027d-101">New-AzsPlan</span></span>

## <span data-ttu-id="8027d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8027d-102">SYNOPSIS</span></span>
<span data-ttu-id="8027d-103">Erstellt einen neuen Plan</span><span class="sxs-lookup"><span data-stu-id="8027d-103">Creates a new plan</span></span>

## <span data-ttu-id="8027d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8027d-104">SYNTAX</span></span>

```
New-AzsPlan [-Name] <String> [-ResourceGroupName] <String> [-DisplayName] <String> [-QuotaIds] <String[]>
 [[-Description] <String>] [[-SkuIds] <String[]>] [[-ExternalReferenceId] <String>] [[-Location] <String>]
 [[-SubscriptionCount] <Int64>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8027d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8027d-105">DESCRIPTION</span></span>
<span data-ttu-id="8027d-106">Erstellt einen neuen Plan</span><span class="sxs-lookup"><span data-stu-id="8027d-106">Creates a new plan</span></span>

## <span data-ttu-id="8027d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8027d-107">EXAMPLES</span></span>

### <span data-ttu-id="8027d-108">--------------------------Beispiel 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8027d-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsPlan -Name "plan1" -ResourceGroupName "rg1" -QuotaIds "/subscriptions/0a823c45-d9e7-4812-a138-74e22213693a/providers/Microsoft.Subscriptions.Admin/locations/local/quotas/delegatedProviderQuota" -Location "local" -DisplayName "plan1" -Description "asda"
```

<span data-ttu-id="8027d-109">Erstellt einen neuen Plan</span><span class="sxs-lookup"><span data-stu-id="8027d-109">Creates a new plan</span></span>

## <span data-ttu-id="8027d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8027d-110">PARAMETERS</span></span>

### <span data-ttu-id="8027d-111">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8027d-111">-Description</span></span>
<span data-ttu-id="8027d-112">Beschreibung des Plans</span><span class="sxs-lookup"><span data-stu-id="8027d-112">Description of the plan.</span></span>

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

### <span data-ttu-id="8027d-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8027d-113">-DisplayName</span></span>
<span data-ttu-id="8027d-114">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="8027d-114">Display name.</span></span>

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

### <span data-ttu-id="8027d-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="8027d-115">-ExternalReferenceId</span></span>
<span data-ttu-id="8027d-116">Externer Verweisbezeichner.</span><span class="sxs-lookup"><span data-stu-id="8027d-116">External reference identifier.</span></span>

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

### <span data-ttu-id="8027d-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="8027d-117">-Location</span></span>
<span data-ttu-id="8027d-118">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="8027d-118">Location of the resource.</span></span>

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

### <span data-ttu-id="8027d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="8027d-119">-Name</span></span>
<span data-ttu-id="8027d-120">Der Name des Plans.</span><span class="sxs-lookup"><span data-stu-id="8027d-120">Name of the plan.</span></span>

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

### <span data-ttu-id="8027d-121">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="8027d-121">-QuotaIds</span></span>
<span data-ttu-id="8027d-122">Kontingent Bezeichner im Plan.</span><span class="sxs-lookup"><span data-stu-id="8027d-122">Quota identifiers under the plan.</span></span>

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

### <span data-ttu-id="8027d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8027d-123">-ResourceGroupName</span></span>
<span data-ttu-id="8027d-124">Die Ressourcengruppe, unter der sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="8027d-124">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="8027d-125">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="8027d-125">-SkuIds</span></span>
<span data-ttu-id="8027d-126">SKU-IDs.</span><span class="sxs-lookup"><span data-stu-id="8027d-126">SKU identifiers.</span></span>

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

### <span data-ttu-id="8027d-127">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="8027d-127">-SubscriptionCount</span></span>
<span data-ttu-id="8027d-128">Anzahl der Abonnements</span><span class="sxs-lookup"><span data-stu-id="8027d-128">Subscription count.</span></span>

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

### <span data-ttu-id="8027d-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8027d-129">-Confirm</span></span>
<span data-ttu-id="8027d-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8027d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8027d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8027d-131">-WhatIf</span></span>
<span data-ttu-id="8027d-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8027d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8027d-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8027d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8027d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8027d-134">CommonParameters</span></span>
<span data-ttu-id="8027d-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8027d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8027d-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8027d-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8027d-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8027d-137">INPUTS</span></span>

## <span data-ttu-id="8027d-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8027d-138">OUTPUTS</span></span>

### <span data-ttu-id="8027d-139">Microsoft. AzureStack. Management. Subscriptions. admin. Models. Plan</span><span class="sxs-lookup"><span data-stu-id="8027d-139">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="8027d-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="8027d-140">NOTES</span></span>

## <span data-ttu-id="8027d-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8027d-141">RELATED LINKS</span></span>

