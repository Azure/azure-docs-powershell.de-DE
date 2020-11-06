---
external help file: Microsoft.Azure.Commands.MarketplaceOrdering.dll-Help.xml
Module Name: AzureRM.MarketplaceOrdering
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
ms.openlocfilehash: 843bb68c5aebc18af60e1cc74915b269738059f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504886"
---
# <span data-ttu-id="d5b8a-101">Set-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="d5b8a-101">Set-AzureRmMarketplaceTerms</span></span>

## <span data-ttu-id="d5b8a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d5b8a-102">SYNOPSIS</span></span>
<span data-ttu-id="d5b8a-103">Akzeptieren oder ablehnen von Ausdrücken für eine bestimmte Publisher-ID (Publisher), Angebots-ID (Produkt) und Plan-ID (Name).</span><span class="sxs-lookup"><span data-stu-id="d5b8a-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="d5b8a-104">Bitte verwenden Sie Get-AzureRmMarketplaceTerms, um die Vertragsbedingungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d5b8a-104">Please use Get-AzureRmMarketplaceTerms to get the agreement terms.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5b8a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5b8a-105">SYNTAX</span></span>

### <span data-ttu-id="d5b8a-106">AgreementAcceptParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d5b8a-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d5b8a-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5b8a-107">AgreementRejectParameterSet</span></span>
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d5b8a-108">InputObjectAcceptParametrSet</span><span class="sxs-lookup"><span data-stu-id="d5b8a-108">InputObjectAcceptParametrSet</span></span>
```
Set-AzureRmMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5b8a-109">InputObjectRejectParametrSet</span><span class="sxs-lookup"><span data-stu-id="d5b8a-109">InputObjectRejectParametrSet</span></span>
```
Set-AzureRmMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5b8a-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d5b8a-110">DESCRIPTION</span></span>
<span data-ttu-id="d5b8a-111">Das Cmdlet " **Satz-AzureRmMarketplaceTerms** " speichert das Ausdrücke-Objekt für die angegebene Publisher-ID (Publisher), Angebots-ID (Produkt) und Plan-ID (Name)-Tupel.</span><span class="sxs-lookup"><span data-stu-id="d5b8a-111">The **Set-AzureRmMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="d5b8a-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d5b8a-112">EXAMPLES</span></span>

### <span data-ttu-id="d5b8a-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d5b8a-113">Example 1</span></span>
```
PS C:\> Set-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```

### <span data-ttu-id="d5b8a-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d5b8a-114">Example 2</span></span>
```
PS C:\> Get-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzureRmMarketplaceTerms -Accept
```

## <span data-ttu-id="d5b8a-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5b8a-115">PARAMETERS</span></span>

### <span data-ttu-id="d5b8a-116">– Akzeptieren</span><span class="sxs-lookup"><span data-stu-id="d5b8a-116">-Accept</span></span>
<span data-ttu-id="d5b8a-117">Geben Sie diese an, um die rechtlichen Best imbegriffe zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="d5b8a-117">Pass this to accept the legal terms.</span></span>

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

### <span data-ttu-id="d5b8a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5b8a-118">-DefaultProfile</span></span>
<span data-ttu-id="d5b8a-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d5b8a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d5b8a-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d5b8a-120">-InputObject</span></span>
<span data-ttu-id="d5b8a-121">In Get-AzureRmMarketplaceTerms-Cmdlet zurückgegebene Ausdrücke-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d5b8a-121">Terms object returned in Get-AzureRmMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="d5b8a-122">Dies ist ein obligatorischer Parameter, wenn Accepted Parameter wahr ist.</span><span class="sxs-lookup"><span data-stu-id="d5b8a-122">This is a mandatory parameter if Accepted paramter is true.</span></span>

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

### <span data-ttu-id="d5b8a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="d5b8a-123">-Name</span></span>
<span data-ttu-id="d5b8a-124">Plan-Identifier-Zeichenfolge des bereitzustellenden Bilds</span><span class="sxs-lookup"><span data-stu-id="d5b8a-124">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="d5b8a-125">-Product</span><span class="sxs-lookup"><span data-stu-id="d5b8a-125">-Product</span></span>
<span data-ttu-id="d5b8a-126">Angebots Kennungszeichenfolge des bereitzustellenden Bilds.</span><span class="sxs-lookup"><span data-stu-id="d5b8a-126">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="d5b8a-127">-Publisher</span><span class="sxs-lookup"><span data-stu-id="d5b8a-127">-Publisher</span></span>
<span data-ttu-id="d5b8a-128">Herausgeber Kennungszeichenfolge des bereitzustellenden Bilds.</span><span class="sxs-lookup"><span data-stu-id="d5b8a-128">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="d5b8a-129">-Ablehnen</span><span class="sxs-lookup"><span data-stu-id="d5b8a-129">-Reject</span></span>
<span data-ttu-id="d5b8a-130">Übergeben Sie diese, um die rechtlichen Best imbegriffe abzulehnen.</span><span class="sxs-lookup"><span data-stu-id="d5b8a-130">Pass this to reject the legal terms.</span></span>

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

### <span data-ttu-id="d5b8a-131">-AGB</span><span class="sxs-lookup"><span data-stu-id="d5b8a-131">-Terms</span></span>
<span data-ttu-id="d5b8a-132">In Get-AzureRmMarketplaceTerms-Cmdlet zurückgegebene Ausdrücke-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d5b8a-132">Terms object returned in Get-AzureRmMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="d5b8a-133">Dies ist ein obligatorischer Parameter, wenn Accepted Parameter wahr ist.</span><span class="sxs-lookup"><span data-stu-id="d5b8a-133">This is a mandatory parameter if Accepted paramter is true.</span></span>

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

### <span data-ttu-id="d5b8a-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d5b8a-134">-Confirm</span></span>
<span data-ttu-id="d5b8a-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d5b8a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5b8a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5b8a-136">-WhatIf</span></span>
<span data-ttu-id="d5b8a-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d5b8a-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d5b8a-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d5b8a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5b8a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5b8a-139">CommonParameters</span></span>
<span data-ttu-id="d5b8a-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5b8a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5b8a-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5b8a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5b8a-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d5b8a-142">INPUTS</span></span>

### <span data-ttu-id="d5b8a-143">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="d5b8a-143">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>
<span data-ttu-id="d5b8a-144">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="d5b8a-144">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="d5b8a-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d5b8a-145">OUTPUTS</span></span>

### <span data-ttu-id="d5b8a-146">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="d5b8a-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>
<span data-ttu-id="d5b8a-147">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="d5b8a-147">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="d5b8a-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="d5b8a-148">NOTES</span></span>

## <span data-ttu-id="d5b8a-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d5b8a-149">RELATED LINKS</span></span>

