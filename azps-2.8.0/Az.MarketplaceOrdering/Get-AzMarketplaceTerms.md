---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering/get-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
ms.openlocfilehash: 730861b055259fd0aee5490de2421abe96afc10b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650612"
---
# <span data-ttu-id="a330b-101">Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="a330b-101">Get-AzMarketplaceTerms</span></span>

## <span data-ttu-id="a330b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a330b-102">SYNOPSIS</span></span>
<span data-ttu-id="a330b-103">Besorgen Sie sich die Vertragsbedingungen für eine bestimmte Publisher-ID (Publisher), Angebots-ID (Produkt) und Plan-ID (Name).</span><span class="sxs-lookup"><span data-stu-id="a330b-103">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="a330b-104">Die von diesem Befehl zurückgegebenen Ausdrücke-Objekte sollten an Set-AzMarketplaceTerms übergeben werden, um die rechtlichen Best imbegriffe zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="a330b-104">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

## <span data-ttu-id="a330b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a330b-105">SYNTAX</span></span>

```
Get-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a330b-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a330b-106">DESCRIPTION</span></span>
<span data-ttu-id="a330b-107">Das Cmdlet " **Get-AzMarketplaceTerms** " gibt die Bedingungen für die angegebene Publisher-ID (Publisher), die Angebots-ID (Produkt) und den Plan-ID (Name)-Tupel zurück.</span><span class="sxs-lookup"><span data-stu-id="a330b-107">The **Get-AzMarketplaceTerms** cmdlet returns terms for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="a330b-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a330b-108">EXAMPLES</span></span>

### <span data-ttu-id="a330b-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a330b-109">Example 1</span></span>
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

## <span data-ttu-id="a330b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a330b-110">PARAMETERS</span></span>

### <span data-ttu-id="a330b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a330b-111">-DefaultProfile</span></span>
<span data-ttu-id="a330b-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a330b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a330b-113">-Name</span><span class="sxs-lookup"><span data-stu-id="a330b-113">-Name</span></span>
<span data-ttu-id="a330b-114">Plan-Identifier-Zeichenfolge des bereitzustellenden Bilds</span><span class="sxs-lookup"><span data-stu-id="a330b-114">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="a330b-115">-Product</span><span class="sxs-lookup"><span data-stu-id="a330b-115">-Product</span></span>
<span data-ttu-id="a330b-116">Angebots Kennungszeichenfolge des bereitzustellenden Bilds.</span><span class="sxs-lookup"><span data-stu-id="a330b-116">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="a330b-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="a330b-117">-Publisher</span></span>
<span data-ttu-id="a330b-118">Herausgeber Kennungszeichenfolge des bereitzustellenden Bilds.</span><span class="sxs-lookup"><span data-stu-id="a330b-118">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="a330b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a330b-119">CommonParameters</span></span>
<span data-ttu-id="a330b-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a330b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a330b-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a330b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a330b-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a330b-122">INPUTS</span></span>

### <span data-ttu-id="a330b-123">Keine</span><span class="sxs-lookup"><span data-stu-id="a330b-123">None</span></span>

## <span data-ttu-id="a330b-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a330b-124">OUTPUTS</span></span>

### <span data-ttu-id="a330b-125">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="a330b-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="a330b-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="a330b-126">NOTES</span></span>

## <span data-ttu-id="a330b-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a330b-127">RELATED LINKS</span></span>
