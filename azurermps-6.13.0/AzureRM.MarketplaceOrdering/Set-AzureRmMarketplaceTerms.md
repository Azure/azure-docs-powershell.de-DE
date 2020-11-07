---
external help file: Microsoft.Azure.Commands.MarketplaceOrdering.dll-Help.xml
Module Name: AzureRM.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.marketplaceordering/set-azurermmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
ms.openlocfilehash: 7932a733fcd672d8ee92e6452765745281ee0a2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662450"
---
# <span data-ttu-id="e1443-101">Set-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="e1443-101">Set-AzureRmMarketplaceTerms</span></span>

## <span data-ttu-id="e1443-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e1443-102">SYNOPSIS</span></span>
<span data-ttu-id="e1443-103">Akzeptieren oder ablehnen von Ausdrücken für eine bestimmte Publisher-ID (Publisher), Angebots-ID (Produkt) und Plan-ID (Name).</span><span class="sxs-lookup"><span data-stu-id="e1443-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="e1443-104">Bitte verwenden Sie Get-AzureRmMarketplaceTerms, um die Vertragsbedingungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e1443-104">Please use Get-AzureRmMarketplaceTerms to get the agreement terms.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1443-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1443-105">SYNTAX</span></span>

### <span data-ttu-id="e1443-106">AgreementAcceptParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e1443-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e1443-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1443-107">AgreementRejectParameterSet</span></span>
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e1443-108">InputObjectAcceptParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1443-108">InputObjectAcceptParameterSet</span></span>
```
Set-AzureRmMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1443-109">InputObjectRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e1443-109">InputObjectRejectParameterSet</span></span>
```
Set-AzureRmMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1443-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e1443-110">DESCRIPTION</span></span>
<span data-ttu-id="e1443-111">Das Cmdlet " **Satz-AzureRmMarketplaceTerms** " speichert das Ausdrücke-Objekt für die angegebene Publisher-ID (Publisher), Angebots-ID (Produkt) und Plan-ID (Name)-Tupel.</span><span class="sxs-lookup"><span data-stu-id="e1443-111">The **Set-AzureRmMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="e1443-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e1443-112">EXAMPLES</span></span>

### <span data-ttu-id="e1443-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e1443-113">Example 1</span></span>
<span data-ttu-id="e1443-114">Abrufen des Marketplace Publisher-Vertrags</span><span class="sxs-lookup"><span data-stu-id="e1443-114">Get the marketplace publisher agreement</span></span>
```
PS C:\> Get-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzureRmMarketplaceTerms -Accept
```

### <span data-ttu-id="e1443-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e1443-115">Example 2</span></span>
<span data-ttu-id="e1443-116">Stellen Sie die Publisher-Vereinbarung auf "akzeptieren" ein.</span><span class="sxs-lookup"><span data-stu-id="e1443-116">Set the publisher agreement to 'Accept'.</span></span> <span data-ttu-id="e1443-117">Abrufen des Werts für den "Termes"-Parameter aus dem Cmdlet "Get-AzureRmMarketplaceTerms"</span><span class="sxs-lookup"><span data-stu-id="e1443-117">Get the value for the 'Terms' parameter from the 'Get-AzureRmMarketplaceTerms' cmdlet</span></span>
```
PS C:\> Set-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```


## <span data-ttu-id="e1443-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1443-118">PARAMETERS</span></span>

### <span data-ttu-id="e1443-119">– Akzeptieren</span><span class="sxs-lookup"><span data-stu-id="e1443-119">-Accept</span></span>
<span data-ttu-id="e1443-120">Geben Sie diese an, um die rechtlichen Best imbegriffe zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="e1443-120">Pass this to accept the legal terms.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AgreementAcceptParameterSet, InputObjectAcceptParametrSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1443-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1443-121">-DefaultProfile</span></span>
<span data-ttu-id="e1443-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e1443-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1443-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e1443-123">-InputObject</span></span>
<span data-ttu-id="e1443-124">In Get-AzureRmMarketplaceTerms-Cmdlet zurückgegebene Ausdrücke-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e1443-124">Terms object returned in Get-AzureRmMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="e1443-125">Dies ist ein obligatorischer Parameter, wenn Accepted Parameter wahr ist.</span><span class="sxs-lookup"><span data-stu-id="e1443-125">This is a mandatory parameter if Accepted paramter is true.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms
Parameter Sets: InputObjectAcceptParametrSet, InputObjectRejectParametrSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1443-126">-Name</span><span class="sxs-lookup"><span data-stu-id="e1443-126">-Name</span></span>
<span data-ttu-id="e1443-127">Plan-Identifier-Zeichenfolge des bereitzustellenden Bilds</span><span class="sxs-lookup"><span data-stu-id="e1443-127">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="e1443-128">-Product</span><span class="sxs-lookup"><span data-stu-id="e1443-128">-Product</span></span>
<span data-ttu-id="e1443-129">Angebots Kennungszeichenfolge des bereitzustellenden Bilds.</span><span class="sxs-lookup"><span data-stu-id="e1443-129">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="e1443-130">-Publisher</span><span class="sxs-lookup"><span data-stu-id="e1443-130">-Publisher</span></span>
<span data-ttu-id="e1443-131">Herausgeber Kennungszeichenfolge des bereitzustellenden Bilds.</span><span class="sxs-lookup"><span data-stu-id="e1443-131">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="e1443-132">-Ablehnen</span><span class="sxs-lookup"><span data-stu-id="e1443-132">-Reject</span></span>
<span data-ttu-id="e1443-133">Übergeben Sie diese, um die rechtlichen Best imbegriffe abzulehnen.</span><span class="sxs-lookup"><span data-stu-id="e1443-133">Pass this to reject the legal terms.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AgreementRejectParameterSet, InputObjectRejectParametrSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1443-134">-AGB</span><span class="sxs-lookup"><span data-stu-id="e1443-134">-Terms</span></span>
<span data-ttu-id="e1443-135">In Get-AzureRmMarketplaceTerms-Cmdlet zurückgegebene Ausdrücke-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e1443-135">Terms object returned in Get-AzureRmMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="e1443-136">Dies ist ein obligatorischer Parameter, wenn Accepted Parameter wahr ist.</span><span class="sxs-lookup"><span data-stu-id="e1443-136">This is a mandatory parameter if Accepted paramter is true.</span></span>

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

### <span data-ttu-id="e1443-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e1443-137">-Confirm</span></span>
<span data-ttu-id="e1443-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e1443-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1443-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1443-139">-WhatIf</span></span>
<span data-ttu-id="e1443-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e1443-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e1443-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e1443-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1443-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1443-142">CommonParameters</span></span>
<span data-ttu-id="e1443-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1443-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1443-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1443-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1443-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e1443-145">INPUTS</span></span>

### <span data-ttu-id="e1443-146">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="e1443-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>
<span data-ttu-id="e1443-147">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e1443-147">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="e1443-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e1443-148">OUTPUTS</span></span>

### <span data-ttu-id="e1443-149">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="e1443-149">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="e1443-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="e1443-150">NOTES</span></span>

## <span data-ttu-id="e1443-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e1443-151">RELATED LINKS</span></span>
