---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering/set-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
ms.openlocfilehash: fb40d1c103da1cc9f1cfe306ebdaab5abf6ec316
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147489"
---
# <span data-ttu-id="fd051-101">Set-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="fd051-101">Set-AzMarketplaceTerms</span></span>

## <span data-ttu-id="fd051-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd051-102">SYNOPSIS</span></span>
<span data-ttu-id="fd051-103">Akzeptieren oder ablehnen Sie Bedingungen für eine bestimmte Herausgeber-ID(Herausgeber), Angebots-ID(Produkt) und Plan-ID(Name).</span><span class="sxs-lookup"><span data-stu-id="fd051-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="fd051-104">Verwenden Sie Get-AzMarketplaceTerms, um die Bedingungen des Vertrags zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="fd051-104">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>

## <span data-ttu-id="fd051-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fd051-105">SYNTAX</span></span>

### <span data-ttu-id="fd051-106">AgreementAcceptParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fd051-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd051-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd051-107">AgreementRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd051-108">InputObjectAcceptParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd051-108">InputObjectAcceptParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd051-109">InputObjectRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd051-109">InputObjectRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd051-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fd051-110">DESCRIPTION</span></span>
<span data-ttu-id="fd051-111">Das **Cmdlet "Set-AzMarketplaceTerms"** speichert das Objekt "terms" für ein angegebenes Publisher-ID(Publisher-), Angebots-ID(Produkt) und Plan-ID(Name)-Tupel.</span><span class="sxs-lookup"><span data-stu-id="fd051-111">The **Set-AzMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="fd051-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fd051-112">EXAMPLES</span></span>

### <span data-ttu-id="fd051-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fd051-113">Example 1</span></span>
<span data-ttu-id="fd051-114">Herausgebervertrag für Marketplace</span><span class="sxs-lookup"><span data-stu-id="fd051-114">Get the marketplace publisher agreement</span></span>


```
PS C:\> Get-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzMarketplaceTerms -Accept
```

### <span data-ttu-id="fd051-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fd051-115">Example 2</span></span>
<span data-ttu-id="fd051-116">Legen Sie den Herausgebervertrag auf "Akzeptieren" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="fd051-116">Set the publisher agreement to 'Accept'.</span></span> <span data-ttu-id="fd051-117">Den Wert für den Parameter "Terms" aus dem Cmdlet "Get-AzMarketplaceTerms"</span><span class="sxs-lookup"><span data-stu-id="fd051-117">Get the value for the 'Terms' parameter from the 'Get-AzMarketplaceTerms' cmdlet</span></span>


```
PS C:\> Set-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```

## <span data-ttu-id="fd051-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd051-118">PARAMETERS</span></span>

### <span data-ttu-id="fd051-119">-Accept</span><span class="sxs-lookup"><span data-stu-id="fd051-119">-Accept</span></span>
<span data-ttu-id="fd051-120">Übergeben Sie dies, um die rechtlichen Bedingungen zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="fd051-120">Pass this to accept the legal terms.</span></span>

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

### <span data-ttu-id="fd051-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd051-121">-DefaultProfile</span></span>
<span data-ttu-id="fd051-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fd051-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd051-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd051-123">-InputObject</span></span>
<span data-ttu-id="fd051-124">Im Cmdlet zurückgegebenes Get-AzMarketplaceTerms Konditionenobjekt.</span><span class="sxs-lookup"><span data-stu-id="fd051-124">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="fd051-125">Dies ist ein obligatorischer Parameter, wenn "Accepted"-Parameter "true" ist.</span><span class="sxs-lookup"><span data-stu-id="fd051-125">This is a mandatory parameter if Accepted parameter is true.</span></span>

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

### <span data-ttu-id="fd051-126">-Name</span><span class="sxs-lookup"><span data-stu-id="fd051-126">-Name</span></span>
<span data-ttu-id="fd051-127">Planen Sie die Zeichenfolge des bereitgestellten Bilds.</span><span class="sxs-lookup"><span data-stu-id="fd051-127">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="fd051-128">-Produkt</span><span class="sxs-lookup"><span data-stu-id="fd051-128">-Product</span></span>
<span data-ttu-id="fd051-129">Angebotsbezeichnerzeichenfolge des bereitgestellten Bilds.</span><span class="sxs-lookup"><span data-stu-id="fd051-129">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="fd051-130">-Publisher</span><span class="sxs-lookup"><span data-stu-id="fd051-130">-Publisher</span></span>
<span data-ttu-id="fd051-131">Herausgeberbezeichnerzeichenfolge des bereitgestellten Bilds.</span><span class="sxs-lookup"><span data-stu-id="fd051-131">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="fd051-132">-Reject</span><span class="sxs-lookup"><span data-stu-id="fd051-132">-Reject</span></span>
<span data-ttu-id="fd051-133">Übergeben Sie dies, um die rechtlichen Bedingungen abzulehnen.</span><span class="sxs-lookup"><span data-stu-id="fd051-133">Pass this to reject the legal terms.</span></span>

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

### <span data-ttu-id="fd051-134">-Bedingungen</span><span class="sxs-lookup"><span data-stu-id="fd051-134">-Terms</span></span>
<span data-ttu-id="fd051-135">Im Cmdlet zurückgegebenes Get-AzMarketplaceTerms Konditionenobjekt.</span><span class="sxs-lookup"><span data-stu-id="fd051-135">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="fd051-136">Dies ist ein obligatorischer Parameter, wenn "Accepted"-Parameter "true" ist.</span><span class="sxs-lookup"><span data-stu-id="fd051-136">This is a mandatory parameter if Accepted parameter is true.</span></span>

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

### <span data-ttu-id="fd051-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd051-137">-Confirm</span></span>
<span data-ttu-id="fd051-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fd051-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd051-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fd051-139">-WhatIf</span></span>
<span data-ttu-id="fd051-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fd051-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd051-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fd051-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd051-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd051-142">CommonParameters</span></span>
<span data-ttu-id="fd051-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd051-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd051-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd051-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd051-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fd051-145">INPUTS</span></span>

### <span data-ttu-id="fd051-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="fd051-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="fd051-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fd051-147">OUTPUTS</span></span>

### <span data-ttu-id="fd051-148">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="fd051-148">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="fd051-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fd051-149">NOTES</span></span>

## <span data-ttu-id="fd051-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fd051-150">RELATED LINKS</span></span>
