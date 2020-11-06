---
external help file: Microsoft.Azure.Commands.MarketplaceOrdering.dll-Help.xml
Module Name: AzureRM.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.marketplaceordering/set-azurermmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
ms.openlocfilehash: 33662eed86e5ad7269c81694bc92cd2bf27f93cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478457"
---
# <span data-ttu-id="2ec71-101">Set-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="2ec71-101">Set-AzureRmMarketplaceTerms</span></span>

## <span data-ttu-id="2ec71-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2ec71-102">SYNOPSIS</span></span>
<span data-ttu-id="2ec71-103">Akzeptieren oder ablehnen von Ausdrücken für eine bestimmte Publisher-ID (Publisher), Angebots-ID (Produkt) und Plan-ID (Name).</span><span class="sxs-lookup"><span data-stu-id="2ec71-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="2ec71-104">Bitte verwenden Sie Get-AzureRmMarketplaceTerms, um die Vertragsbedingungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2ec71-104">Please use Get-AzureRmMarketplaceTerms to get the agreement terms.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ec71-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ec71-105">SYNTAX</span></span>

### <span data-ttu-id="2ec71-106">AgreementAcceptParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2ec71-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2ec71-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ec71-107">AgreementRejectParameterSet</span></span>
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2ec71-108">InputObjectAcceptParametrSet</span><span class="sxs-lookup"><span data-stu-id="2ec71-108">InputObjectAcceptParametrSet</span></span>
```
Set-AzureRmMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ec71-109">InputObjectRejectParametrSet</span><span class="sxs-lookup"><span data-stu-id="2ec71-109">InputObjectRejectParametrSet</span></span>
```
Set-AzureRmMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ec71-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2ec71-110">DESCRIPTION</span></span>
<span data-ttu-id="2ec71-111">Das Cmdlet " **Satz-AzureRmMarketplaceTerms** " speichert das Ausdrücke-Objekt für die angegebene Publisher-ID (Publisher), Angebots-ID (Produkt) und Plan-ID (Name)-Tupel.</span><span class="sxs-lookup"><span data-stu-id="2ec71-111">The **Set-AzureRmMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="2ec71-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2ec71-112">EXAMPLES</span></span>

### <span data-ttu-id="2ec71-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2ec71-113">Example 1</span></span>
```
PS C:\> Set-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```

### <span data-ttu-id="2ec71-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2ec71-114">Example 2</span></span>
```
PS C:\> Get-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzureRmMarketplaceTerms -Accept
```

## <span data-ttu-id="2ec71-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ec71-115">PARAMETERS</span></span>

### <span data-ttu-id="2ec71-116">– Akzeptieren</span><span class="sxs-lookup"><span data-stu-id="2ec71-116">-Accept</span></span>
<span data-ttu-id="2ec71-117">Geben Sie diese an, um die rechtlichen Best imbegriffe zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="2ec71-117">Pass this to accept the legal terms.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AgreementAcceptParameterSet, InputObjectAcceptParametrSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ec71-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ec71-118">-DefaultProfile</span></span>
<span data-ttu-id="2ec71-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2ec71-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ec71-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2ec71-120">-InputObject</span></span>
<span data-ttu-id="2ec71-121">In Get-AzureRmMarketplaceTerms-Cmdlet zurückgegebene Ausdrücke-Objekt.</span><span class="sxs-lookup"><span data-stu-id="2ec71-121">Terms object returned in Get-AzureRmMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="2ec71-122">Dies ist ein obligatorischer Parameter, wenn Accepted Parameter wahr ist.</span><span class="sxs-lookup"><span data-stu-id="2ec71-122">This is a mandatory parameter if Accepted paramter is true.</span></span>

```yaml
Type: PSAgreementTerms
Parameter Sets: InputObjectAcceptParametrSet, InputObjectRejectParametrSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ec71-123">-Name</span><span class="sxs-lookup"><span data-stu-id="2ec71-123">-Name</span></span>
<span data-ttu-id="2ec71-124">Plan-Identifier-Zeichenfolge des bereitzustellenden Bilds</span><span class="sxs-lookup"><span data-stu-id="2ec71-124">Plan identifier string of image being deployed.</span></span>

```yaml
Type: String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ec71-125">-Product</span><span class="sxs-lookup"><span data-stu-id="2ec71-125">-Product</span></span>
<span data-ttu-id="2ec71-126">Angebots Kennungszeichenfolge des bereitzustellenden Bilds.</span><span class="sxs-lookup"><span data-stu-id="2ec71-126">Offer identifier string of image being deployed.</span></span>

```yaml
Type: String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ec71-127">-Publisher</span><span class="sxs-lookup"><span data-stu-id="2ec71-127">-Publisher</span></span>
<span data-ttu-id="2ec71-128">Herausgeber Kennungszeichenfolge des bereitzustellenden Bilds.</span><span class="sxs-lookup"><span data-stu-id="2ec71-128">Publisher identifier string of image being deployed.</span></span>

```yaml
Type: String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ec71-129">-Ablehnen</span><span class="sxs-lookup"><span data-stu-id="2ec71-129">-Reject</span></span>
<span data-ttu-id="2ec71-130">Übergeben Sie diese, um die rechtlichen Best imbegriffe abzulehnen.</span><span class="sxs-lookup"><span data-stu-id="2ec71-130">Pass this to reject the legal terms.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AgreementRejectParameterSet, InputObjectRejectParametrSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ec71-131">-AGB</span><span class="sxs-lookup"><span data-stu-id="2ec71-131">-Terms</span></span>
<span data-ttu-id="2ec71-132">In Get-AzureRmMarketplaceTerms-Cmdlet zurückgegebene Ausdrücke-Objekt.</span><span class="sxs-lookup"><span data-stu-id="2ec71-132">Terms object returned in Get-AzureRmMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="2ec71-133">Dies ist ein obligatorischer Parameter, wenn Accepted Parameter wahr ist.</span><span class="sxs-lookup"><span data-stu-id="2ec71-133">This is a mandatory parameter if Accepted paramter is true.</span></span>

```yaml
Type: PSAgreementTerms
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ec71-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2ec71-134">-Confirm</span></span>
<span data-ttu-id="2ec71-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2ec71-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ec71-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ec71-136">-WhatIf</span></span>
<span data-ttu-id="2ec71-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2ec71-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2ec71-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2ec71-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ec71-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ec71-139">CommonParameters</span></span>
<span data-ttu-id="2ec71-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ec71-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ec71-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ec71-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ec71-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2ec71-142">INPUTS</span></span>

### <span data-ttu-id="2ec71-143">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="2ec71-143">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>
<span data-ttu-id="2ec71-144">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="2ec71-144">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="2ec71-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2ec71-145">OUTPUTS</span></span>

### <span data-ttu-id="2ec71-146">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="2ec71-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>
<span data-ttu-id="2ec71-147">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="2ec71-147">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="2ec71-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="2ec71-148">NOTES</span></span>

## <span data-ttu-id="2ec71-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2ec71-149">RELATED LINKS</span></span>

