---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/powershell/module/az.marketplaceordering/set-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
ms.openlocfilehash: b4098481db78bf045abad04aee4e2e5076f71ce1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918779"
---
# <span data-ttu-id="28f84-101">Set-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="28f84-101">Set-AzMarketplaceTerms</span></span>

## <span data-ttu-id="28f84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28f84-102">SYNOPSIS</span></span>
<span data-ttu-id="28f84-103">Akzeptieren oder Ablehnen von Bedingungen für eine bestimmte Herausgeber-ID(Publisher), Angebots-ID(Produkt) und Plan-ID(Name).</span><span class="sxs-lookup"><span data-stu-id="28f84-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="28f84-104">Verwenden Sie Get-AzMarketplaceTerms, um die Vertragsbedingungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="28f84-104">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>

## <span data-ttu-id="28f84-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="28f84-105">SYNTAX</span></span>

### <span data-ttu-id="28f84-106">AgreementAcceptParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="28f84-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="28f84-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="28f84-107">AgreementRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="28f84-108">InputObjectAcceptParameterSet</span><span class="sxs-lookup"><span data-stu-id="28f84-108">InputObjectAcceptParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28f84-109">InputObjectRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="28f84-109">InputObjectRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28f84-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="28f84-110">DESCRIPTION</span></span>
<span data-ttu-id="28f84-111">Das **Cmdlet Set-AzMarketplaceTerms** speichert das Konditionenobjekt für bestimmte Publisher-ID(Publisher), Offer-ID(Produkt) und Plan-ID(Name)-Tupel.</span><span class="sxs-lookup"><span data-stu-id="28f84-111">The **Set-AzMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="28f84-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="28f84-112">EXAMPLES</span></span>

### <span data-ttu-id="28f84-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="28f84-113">Example 1</span></span>
<span data-ttu-id="28f84-114">Holen Sie sich den Marketplace Publisher-Vertrag</span><span class="sxs-lookup"><span data-stu-id="28f84-114">Get the marketplace publisher agreement</span></span>


```
PS C:\> Get-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzMarketplaceTerms -Accept
```

### <span data-ttu-id="28f84-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="28f84-115">Example 2</span></span>
<span data-ttu-id="28f84-116">Legen Sie den Herausgebervertrag auf "Akzeptieren" ein.</span><span class="sxs-lookup"><span data-stu-id="28f84-116">Set the publisher agreement to 'Accept'.</span></span> <span data-ttu-id="28f84-117">Den Wert für den Parameter "Terms" aus dem Cmdlet "Get-AzMarketplaceTerms"</span><span class="sxs-lookup"><span data-stu-id="28f84-117">Get the value for the 'Terms' parameter from the 'Get-AzMarketplaceTerms' cmdlet</span></span>


```
PS C:\> Set-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```

## <span data-ttu-id="28f84-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="28f84-118">PARAMETERS</span></span>

### <span data-ttu-id="28f84-119">-Annehmen</span><span class="sxs-lookup"><span data-stu-id="28f84-119">-Accept</span></span>
<span data-ttu-id="28f84-120">Übergeben Sie dies, um die gesetzlichen Bedingungen zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="28f84-120">Pass this to accept the legal terms.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AgreementAcceptParameterSet, InputObjectAcceptParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28f84-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28f84-121">-DefaultProfile</span></span>
<span data-ttu-id="28f84-122">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="28f84-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28f84-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28f84-123">-InputObject</span></span>
<span data-ttu-id="28f84-124">Im Cmdlet zurückgegebene Get-AzMarketplaceTerms-Objekt.</span><span class="sxs-lookup"><span data-stu-id="28f84-124">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="28f84-125">Dies ist ein obligatorischer Parameter, wenn der Parameter Akzeptiert wahr ist.</span><span class="sxs-lookup"><span data-stu-id="28f84-125">This is a mandatory parameter if Accepted parameter is true.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms
Parameter Sets: InputObjectAcceptParameterSet, InputObjectRejectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28f84-126">-Name</span><span class="sxs-lookup"><span data-stu-id="28f84-126">-Name</span></span>
<span data-ttu-id="28f84-127">Planen Sie die Bezeichnerzeichenfolge des bereitgestellten Bilds.</span><span class="sxs-lookup"><span data-stu-id="28f84-127">Plan identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28f84-128">-Produkt</span><span class="sxs-lookup"><span data-stu-id="28f84-128">-Product</span></span>
<span data-ttu-id="28f84-129">Offer identifier string of image being deployed.</span><span class="sxs-lookup"><span data-stu-id="28f84-129">Offer identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28f84-130">-Publisher</span><span class="sxs-lookup"><span data-stu-id="28f84-130">-Publisher</span></span>
<span data-ttu-id="28f84-131">Publisher-Bezeichnerzeichenfolge des bereitgestellten Bilds.</span><span class="sxs-lookup"><span data-stu-id="28f84-131">Publisher identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28f84-132">-Ablehnen</span><span class="sxs-lookup"><span data-stu-id="28f84-132">-Reject</span></span>
<span data-ttu-id="28f84-133">Übergeben Sie dies, um die gesetzlichen Bedingungen abzulehnen.</span><span class="sxs-lookup"><span data-stu-id="28f84-133">Pass this to reject the legal terms.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AgreementRejectParameterSet, InputObjectRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28f84-134">-Bedingungen</span><span class="sxs-lookup"><span data-stu-id="28f84-134">-Terms</span></span>
<span data-ttu-id="28f84-135">Im Cmdlet zurückgegebene Get-AzMarketplaceTerms-Objekt.</span><span class="sxs-lookup"><span data-stu-id="28f84-135">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="28f84-136">Dies ist ein obligatorischer Parameter, wenn der Parameter Akzeptiert wahr ist.</span><span class="sxs-lookup"><span data-stu-id="28f84-136">This is a mandatory parameter if Accepted parameter is true.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28f84-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="28f84-137">-Confirm</span></span>
<span data-ttu-id="28f84-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="28f84-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28f84-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28f84-139">-WhatIf</span></span>
<span data-ttu-id="28f84-140">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="28f84-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="28f84-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="28f84-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28f84-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28f84-142">CommonParameters</span></span>
<span data-ttu-id="28f84-143">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28f84-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28f84-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28f84-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28f84-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="28f84-145">INPUTS</span></span>

### <span data-ttu-id="28f84-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="28f84-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="28f84-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="28f84-147">OUTPUTS</span></span>

### <span data-ttu-id="28f84-148">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="28f84-148">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="28f84-149">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="28f84-149">NOTES</span></span>

## <span data-ttu-id="28f84-150">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="28f84-150">RELATED LINKS</span></span>
