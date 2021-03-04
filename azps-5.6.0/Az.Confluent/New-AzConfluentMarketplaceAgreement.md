---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/new-azconfluentmarketplaceagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/New-AzConfluentMarketplaceAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/New-AzConfluentMarketplaceAgreement.md
ms.openlocfilehash: f8c293870fa4eeb6f0df8a543473c8a9bda314c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948907"
---
# <span data-ttu-id="69609-101">New-AzConfluentMarketplaceAgreement</span><span class="sxs-lookup"><span data-stu-id="69609-101">New-AzConfluentMarketplaceAgreement</span></span>

## <span data-ttu-id="69609-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69609-102">SYNOPSIS</span></span>
<span data-ttu-id="69609-103">Akzeptieren Sie Marketplace-Bedingungen.</span><span class="sxs-lookup"><span data-stu-id="69609-103">Accept marketplace terms.</span></span>

## <span data-ttu-id="69609-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69609-104">SYNTAX</span></span>

```
New-AzConfluentMarketplaceAgreement [-SubscriptionId <String>] [-Accepted] [-LicenseTextLink <String>]
 [-Plan <String>] [-PrivacyPolicyLink <String>] [-Product <String>] [-Publisher <String>]
 [-RetrieveDatetime <DateTime>] [-Signature <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="69609-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="69609-105">DESCRIPTION</span></span>
<span data-ttu-id="69609-106">Akzeptieren Sie Marketplace-Bedingungen.</span><span class="sxs-lookup"><span data-stu-id="69609-106">Accept marketplace terms.</span></span>

## <span data-ttu-id="69609-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="69609-107">EXAMPLES</span></span>

### <span data-ttu-id="69609-108">Beispiel 1: Erstellen einer vereinbarungskonfluenten Marketplace unter einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="69609-108">Example 1: Create confluent marketplace agreement under a subscription</span></span>
```powershell
PS C:\> New-AzConfluentMarketplaceAgreement -Accepted

Name    Type
----    ----
default Microsoft.Confluent/agreement
```

<span data-ttu-id="69609-109">Mit diesem Befehl wird eine konfluente Marketplace-Vereinbarung unter einem Abonnement erstellt.</span><span class="sxs-lookup"><span data-stu-id="69609-109">This command create confluent marketplace agreement under a subscription.</span></span>

## <span data-ttu-id="69609-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="69609-110">PARAMETERS</span></span>

### <span data-ttu-id="69609-111">-Akzeptiert</span><span class="sxs-lookup"><span data-stu-id="69609-111">-Accepted</span></span>
<span data-ttu-id="69609-112">Wenn eine Version der Bedingungen akzeptiert wurde, andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="69609-112">If any version of the terms have been accepted, otherwise false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69609-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69609-113">-DefaultProfile</span></span>
<span data-ttu-id="69609-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="69609-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69609-115">-LicenseTextLink</span><span class="sxs-lookup"><span data-stu-id="69609-115">-LicenseTextLink</span></span>
<span data-ttu-id="69609-116">Link zu HTML mit Microsoft- und Publisher-Bedingungen.</span><span class="sxs-lookup"><span data-stu-id="69609-116">Link to HTML with Microsoft and Publisher terms.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69609-117">-Plan</span><span class="sxs-lookup"><span data-stu-id="69609-117">-Plan</span></span>
<span data-ttu-id="69609-118">Bezeichnerzeichenfolge planen.</span><span class="sxs-lookup"><span data-stu-id="69609-118">Plan identifier string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69609-119">-PrivacyPolicyLink</span><span class="sxs-lookup"><span data-stu-id="69609-119">-PrivacyPolicyLink</span></span>
<span data-ttu-id="69609-120">Link zur Datenschutzrichtlinie des Herausgebers.</span><span class="sxs-lookup"><span data-stu-id="69609-120">Link to the privacy policy of the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69609-121">-Produkt</span><span class="sxs-lookup"><span data-stu-id="69609-121">-Product</span></span>
<span data-ttu-id="69609-122">Produktbezeichnerzeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="69609-122">Product identifier string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69609-123">-Publisher</span><span class="sxs-lookup"><span data-stu-id="69609-123">-Publisher</span></span>
<span data-ttu-id="69609-124">Publisher-Bezeichnerzeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="69609-124">Publisher identifier string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69609-125">-RetrieveDatetime</span><span class="sxs-lookup"><span data-stu-id="69609-125">-RetrieveDatetime</span></span>
<span data-ttu-id="69609-126">Datum und Uhrzeit in UTC, an dem die Bedingungen akzeptiert wurden.</span><span class="sxs-lookup"><span data-stu-id="69609-126">Date and time in UTC of when the terms were accepted.</span></span>
<span data-ttu-id="69609-127">Dies ist leer, wenn "Akzeptiert" falsch ist.</span><span class="sxs-lookup"><span data-stu-id="69609-127">This is empty if Accepted is false.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69609-128">-Signatur</span><span class="sxs-lookup"><span data-stu-id="69609-128">-Signature</span></span>
<span data-ttu-id="69609-129">Signatur der Bedingungen.</span><span class="sxs-lookup"><span data-stu-id="69609-129">Terms signature.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69609-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="69609-130">-SubscriptionId</span></span>
<span data-ttu-id="69609-131">Microsoft Azure-Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="69609-131">Microsoft Azure subscription id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69609-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="69609-132">-Confirm</span></span>
<span data-ttu-id="69609-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="69609-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69609-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69609-134">-WhatIf</span></span>
<span data-ttu-id="69609-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="69609-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69609-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="69609-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69609-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69609-137">CommonParameters</span></span>
<span data-ttu-id="69609-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69609-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69609-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69609-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69609-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="69609-140">INPUTS</span></span>

## <span data-ttu-id="69609-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="69609-141">OUTPUTS</span></span>

### <span data-ttu-id="69609-142">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IConfluentAgreementResource</span><span class="sxs-lookup"><span data-stu-id="69609-142">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IConfluentAgreementResource</span></span>

## <span data-ttu-id="69609-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="69609-143">NOTES</span></span>

<span data-ttu-id="69609-144">ALIASE</span><span class="sxs-lookup"><span data-stu-id="69609-144">ALIASES</span></span>

## <span data-ttu-id="69609-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="69609-145">RELATED LINKS</span></span>

