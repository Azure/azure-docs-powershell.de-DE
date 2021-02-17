---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering/get-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
ms.openlocfilehash: b729eb0ca1c0cc3b051600b59f260ebfb16d6b6e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147492"
---
# <span data-ttu-id="b2cc0-101">Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="b2cc0-101">Get-AzMarketplaceTerms</span></span>

## <span data-ttu-id="b2cc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2cc0-102">SYNOPSIS</span></span>
<span data-ttu-id="b2cc0-103">Erhalten Sie die Vertragsbedingungen für eine bestimmte Herausgeber-ID(Publisher), Angebots-ID(Produkt) und Plan-ID(Name).</span><span class="sxs-lookup"><span data-stu-id="b2cc0-103">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="b2cc0-104">Das von diesem Befehl zurückgegebene Objekt "terms" sollte an die Set-AzMarketplaceTerms die rechtlichen Bedingungen akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="b2cc0-104">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

## <span data-ttu-id="b2cc0-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b2cc0-105">SYNTAX</span></span>

```
Get-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2cc0-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b2cc0-106">DESCRIPTION</span></span>
<span data-ttu-id="b2cc0-107">Das **Cmdlet "Get-AzMarketplaceTerms"** gibt Konditionen für das Tupel "Herausgeber-ID(Herausgeber"), Angebots-ID(Produkt) und Plan-ID(Name)" zurück.</span><span class="sxs-lookup"><span data-stu-id="b2cc0-107">The **Get-AzMarketplaceTerms** cmdlet returns terms for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="b2cc0-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b2cc0-108">EXAMPLES</span></span>

### <span data-ttu-id="b2cc0-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b2cc0-109">Example 1</span></span>
```
PS C:\> Get-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016"
Publisher         : microsoft-ads
Product           : windows-data-science-vm
Plan              : windows2016
LicenseTextLink   : <LicenseTextLink>
PrivacyPolicyLink : <PrivacyPolicyLink>
Signature         : <Signature>
Accepted          : True
RetrieveDatetime  : <RetrieveDatetime>
```

## <span data-ttu-id="b2cc0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2cc0-110">PARAMETERS</span></span>

### <span data-ttu-id="b2cc0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2cc0-111">-DefaultProfile</span></span>
<span data-ttu-id="b2cc0-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b2cc0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2cc0-113">-Name</span><span class="sxs-lookup"><span data-stu-id="b2cc0-113">-Name</span></span>
<span data-ttu-id="b2cc0-114">Planen Sie die Zeichenfolge des bereitgestellten Bilds.</span><span class="sxs-lookup"><span data-stu-id="b2cc0-114">Plan identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2cc0-115">-Produkt</span><span class="sxs-lookup"><span data-stu-id="b2cc0-115">-Product</span></span>
<span data-ttu-id="b2cc0-116">Angebotsbezeichnerzeichenfolge des bereitgestellten Bilds.</span><span class="sxs-lookup"><span data-stu-id="b2cc0-116">Offer identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2cc0-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="b2cc0-117">-Publisher</span></span>
<span data-ttu-id="b2cc0-118">Herausgeberbezeichnerzeichenfolge des bereitgestellten Bilds.</span><span class="sxs-lookup"><span data-stu-id="b2cc0-118">Publisher identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2cc0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2cc0-119">CommonParameters</span></span>
<span data-ttu-id="b2cc0-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2cc0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2cc0-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2cc0-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2cc0-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b2cc0-122">INPUTS</span></span>

### <span data-ttu-id="b2cc0-123">Keine</span><span class="sxs-lookup"><span data-stu-id="b2cc0-123">None</span></span>

## <span data-ttu-id="b2cc0-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b2cc0-124">OUTPUTS</span></span>

### <span data-ttu-id="b2cc0-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="b2cc0-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="b2cc0-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b2cc0-126">NOTES</span></span>

## <span data-ttu-id="b2cc0-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b2cc0-127">RELATED LINKS</span></span>
