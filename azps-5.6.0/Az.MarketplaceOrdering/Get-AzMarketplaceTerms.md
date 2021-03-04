---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/powershell/module/az.marketplaceordering/get-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
ms.openlocfilehash: 9878bdaa508d2cc229f494dcd53467f9c7d62ed1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925491"
---
# <span data-ttu-id="ebd6b-101">Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="ebd6b-101">Get-AzMarketplaceTerms</span></span>

## <span data-ttu-id="ebd6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebd6b-102">SYNOPSIS</span></span>
<span data-ttu-id="ebd6b-103">Erhalten Sie die Vertragsbedingungen für eine bestimmte Herausgeber-ID(Publisher), Angebots-ID(Produkt) und Plan-ID(Name).</span><span class="sxs-lookup"><span data-stu-id="ebd6b-103">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="ebd6b-104">Das von diesem Befehl zurückgegebene Konditionenobjekt sollte an die Set-AzMarketplaceTerms übergeben werden, um die rechtlichen Bedingungen zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="ebd6b-104">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

## <span data-ttu-id="ebd6b-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ebd6b-105">SYNTAX</span></span>

```
Get-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ebd6b-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ebd6b-106">DESCRIPTION</span></span>
<span data-ttu-id="ebd6b-107">Das **Get-AzMarketplaceTerms-Cmdlet** gibt Konditionen für bestimmte Publisher-ID(Publisher), Offer-ID(Produkt) und Plan-ID(Name)-Tupel zurück.</span><span class="sxs-lookup"><span data-stu-id="ebd6b-107">The **Get-AzMarketplaceTerms** cmdlet returns terms for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="ebd6b-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ebd6b-108">EXAMPLES</span></span>

### <span data-ttu-id="ebd6b-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ebd6b-109">Example 1</span></span>
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

## <span data-ttu-id="ebd6b-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ebd6b-110">PARAMETERS</span></span>

### <span data-ttu-id="ebd6b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebd6b-111">-DefaultProfile</span></span>
<span data-ttu-id="ebd6b-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ebd6b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebd6b-113">-Name</span><span class="sxs-lookup"><span data-stu-id="ebd6b-113">-Name</span></span>
<span data-ttu-id="ebd6b-114">Planen Sie die Bezeichnerzeichenfolge des bereitgestellten Bilds.</span><span class="sxs-lookup"><span data-stu-id="ebd6b-114">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="ebd6b-115">-Produkt</span><span class="sxs-lookup"><span data-stu-id="ebd6b-115">-Product</span></span>
<span data-ttu-id="ebd6b-116">Offer identifier string of image being deployed.</span><span class="sxs-lookup"><span data-stu-id="ebd6b-116">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="ebd6b-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="ebd6b-117">-Publisher</span></span>
<span data-ttu-id="ebd6b-118">Publisher-Bezeichnerzeichenfolge des bereitgestellten Bilds.</span><span class="sxs-lookup"><span data-stu-id="ebd6b-118">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="ebd6b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebd6b-119">CommonParameters</span></span>
<span data-ttu-id="ebd6b-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebd6b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebd6b-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebd6b-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebd6b-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ebd6b-122">INPUTS</span></span>

### <span data-ttu-id="ebd6b-123">Keine</span><span class="sxs-lookup"><span data-stu-id="ebd6b-123">None</span></span>

## <span data-ttu-id="ebd6b-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ebd6b-124">OUTPUTS</span></span>

### <span data-ttu-id="ebd6b-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="ebd6b-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="ebd6b-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ebd6b-126">NOTES</span></span>

## <span data-ttu-id="ebd6b-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ebd6b-127">RELATED LINKS</span></span>
