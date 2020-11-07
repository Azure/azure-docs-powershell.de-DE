---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering/set-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
ms.openlocfilehash: 1cea045bd9b663e542bb435003df79f153542a75
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819079"
---
# <span data-ttu-id="e13fa-101">Set-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="e13fa-101">Set-AzMarketplaceTerms</span></span>

## <span data-ttu-id="e13fa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e13fa-102">SYNOPSIS</span></span>
<span data-ttu-id="e13fa-103">Akzeptieren oder ablehnen von Ausdrücken für eine bestimmte Publisher-ID (Publisher), Angebots-ID (Produkt) und Plan-ID (Name).</span><span class="sxs-lookup"><span data-stu-id="e13fa-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="e13fa-104">Bitte verwenden Sie Get-AzMarketplaceTerms, um die Vertragsbedingungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e13fa-104">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>

## <span data-ttu-id="e13fa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e13fa-105">SYNTAX</span></span>

### <span data-ttu-id="e13fa-106">AgreementAcceptParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e13fa-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e13fa-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e13fa-107">AgreementRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e13fa-108">InputObjectAcceptParameterSet</span><span class="sxs-lookup"><span data-stu-id="e13fa-108">InputObjectAcceptParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e13fa-109">InputObjectRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e13fa-109">InputObjectRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e13fa-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e13fa-110">DESCRIPTION</span></span>
<span data-ttu-id="e13fa-111">Das Cmdlet " **Satz-AzMarketplaceTerms** " speichert das Ausdrücke-Objekt für die angegebene Publisher-ID (Publisher), Angebots-ID (Produkt) und Plan-ID (Name)-Tupel.</span><span class="sxs-lookup"><span data-stu-id="e13fa-111">The **Set-AzMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="e13fa-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e13fa-112">EXAMPLES</span></span>

### <span data-ttu-id="e13fa-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e13fa-113">Example 1</span></span>
<span data-ttu-id="e13fa-114">Abrufen des Marketplace Publisher-Vertrags</span><span class="sxs-lookup"><span data-stu-id="e13fa-114">Get the marketplace publisher agreement</span></span>


```
PS C:\> Get-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzMarketplaceTerms -Accept
```

### <span data-ttu-id="e13fa-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e13fa-115">Example 2</span></span>
<span data-ttu-id="e13fa-116">Stellen Sie die Publisher-Vereinbarung auf "akzeptieren" ein.</span><span class="sxs-lookup"><span data-stu-id="e13fa-116">Set the publisher agreement to 'Accept'.</span></span> <span data-ttu-id="e13fa-117">Abrufen des Werts für den "Termes"-Parameter aus dem Cmdlet "Get-AzMarketplaceTerms"</span><span class="sxs-lookup"><span data-stu-id="e13fa-117">Get the value for the 'Terms' parameter from the 'Get-AzMarketplaceTerms' cmdlet</span></span>


```
PS C:\> Set-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```

## <span data-ttu-id="e13fa-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="e13fa-118">PARAMETERS</span></span>

### <span data-ttu-id="e13fa-119">– Akzeptieren</span><span class="sxs-lookup"><span data-stu-id="e13fa-119">-Accept</span></span>
<span data-ttu-id="e13fa-120">Geben Sie diese an, um die rechtlichen Best imbegriffe zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="e13fa-120">Pass this to accept the legal terms.</span></span>

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

### <span data-ttu-id="e13fa-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e13fa-121">-DefaultProfile</span></span>
<span data-ttu-id="e13fa-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e13fa-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e13fa-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e13fa-123">-InputObject</span></span>
<span data-ttu-id="e13fa-124">In Get-AzMarketplaceTerms-Cmdlet zurückgegebene Ausdrücke-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e13fa-124">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="e13fa-125">Dies ist ein obligatorischer Parameter, wenn Accepted Parameter wahr ist.</span><span class="sxs-lookup"><span data-stu-id="e13fa-125">This is a mandatory parameter if Accepted paramter is true.</span></span>

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

### <span data-ttu-id="e13fa-126">-Name</span><span class="sxs-lookup"><span data-stu-id="e13fa-126">-Name</span></span>
<span data-ttu-id="e13fa-127">Plan-Identifier-Zeichenfolge des bereitzustellenden Bilds</span><span class="sxs-lookup"><span data-stu-id="e13fa-127">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="e13fa-128">-Product</span><span class="sxs-lookup"><span data-stu-id="e13fa-128">-Product</span></span>
<span data-ttu-id="e13fa-129">Angebots Kennungszeichenfolge des bereitzustellenden Bilds.</span><span class="sxs-lookup"><span data-stu-id="e13fa-129">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="e13fa-130">-Publisher</span><span class="sxs-lookup"><span data-stu-id="e13fa-130">-Publisher</span></span>
<span data-ttu-id="e13fa-131">Herausgeber Kennungszeichenfolge des bereitzustellenden Bilds.</span><span class="sxs-lookup"><span data-stu-id="e13fa-131">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="e13fa-132">-Ablehnen</span><span class="sxs-lookup"><span data-stu-id="e13fa-132">-Reject</span></span>
<span data-ttu-id="e13fa-133">Übergeben Sie diese, um die rechtlichen Best imbegriffe abzulehnen.</span><span class="sxs-lookup"><span data-stu-id="e13fa-133">Pass this to reject the legal terms.</span></span>

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

### <span data-ttu-id="e13fa-134">-AGB</span><span class="sxs-lookup"><span data-stu-id="e13fa-134">-Terms</span></span>
<span data-ttu-id="e13fa-135">In Get-AzMarketplaceTerms-Cmdlet zurückgegebene Ausdrücke-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e13fa-135">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="e13fa-136">Dies ist ein obligatorischer Parameter, wenn Accepted Parameter wahr ist.</span><span class="sxs-lookup"><span data-stu-id="e13fa-136">This is a mandatory parameter if Accepted paramter is true.</span></span>

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

### <span data-ttu-id="e13fa-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e13fa-137">-Confirm</span></span>
<span data-ttu-id="e13fa-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e13fa-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e13fa-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e13fa-139">-WhatIf</span></span>
<span data-ttu-id="e13fa-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e13fa-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e13fa-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e13fa-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e13fa-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e13fa-142">CommonParameters</span></span>
<span data-ttu-id="e13fa-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e13fa-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e13fa-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e13fa-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e13fa-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e13fa-145">INPUTS</span></span>

### <span data-ttu-id="e13fa-146">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="e13fa-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="e13fa-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e13fa-147">OUTPUTS</span></span>

### <span data-ttu-id="e13fa-148">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="e13fa-148">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="e13fa-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="e13fa-149">NOTES</span></span>

## <span data-ttu-id="e13fa-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e13fa-150">RELATED LINKS</span></span>
