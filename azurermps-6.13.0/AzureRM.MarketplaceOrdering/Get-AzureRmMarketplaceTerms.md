---
external help file: Microsoft.Azure.Commands.MarketplaceOrdering.dll-Help.xml
Module Name: AzureRM.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.marketplaceordering/get-azurermmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Get-AzureRmMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Get-AzureRmMarketplaceTerms.md
ms.openlocfilehash: f23912ed21105015e69b94b27c5c5cc7899ed044
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479554"
---
# <span data-ttu-id="d0e97-101">Get-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="d0e97-101">Get-AzureRmMarketplaceTerms</span></span>

## <span data-ttu-id="d0e97-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d0e97-102">SYNOPSIS</span></span>
<span data-ttu-id="d0e97-103">Besorgen Sie sich die Vertragsbedingungen für eine bestimmte Publisher-ID (Publisher), Angebots-ID (Produkt) und Plan-ID (Name).</span><span class="sxs-lookup"><span data-stu-id="d0e97-103">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="d0e97-104">Die von diesem Befehl zurückgegebenen Ausdrücke-Objekte sollten an Set-AzureRmMarketplaceTerms übergeben werden, um die rechtlichen Best imbegriffe zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="d0e97-104">The terms object which is returned by this command should be passed to Set-AzureRmMarketplaceTerms to accept the legal terms.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0e97-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0e97-105">SYNTAX</span></span>

```
Get-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0e97-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d0e97-106">DESCRIPTION</span></span>
<span data-ttu-id="d0e97-107">Das Cmdlet " **Get-AzureRmMarketplaceTerms** " gibt die Bedingungen für die angegebene Publisher-ID (Publisher), die Angebots-ID (Produkt) und den Plan-ID (Name)-Tupel zurück.</span><span class="sxs-lookup"><span data-stu-id="d0e97-107">The **Get-AzureRmMarketplaceTerms** cmdlet returns terms for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="d0e97-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d0e97-108">EXAMPLES</span></span>

### <span data-ttu-id="d0e97-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d0e97-109">Example 1</span></span>
```
PS C:\> Get-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016"
Publisher         : microsoft-ads
Product           : windows-data-science-vm
Plan              : windows2016
LicenseTextLink   : <LicenseTextLink>
PrivacyPolicyLink : <PrivacyPolicyLink>
Signature         : <Signature>
Accepted          : True
RetrieveDatetime  : <RetrieveDatetime>
```

## <span data-ttu-id="d0e97-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d0e97-110">PARAMETERS</span></span>

### <span data-ttu-id="d0e97-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0e97-111">-DefaultProfile</span></span>
<span data-ttu-id="d0e97-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d0e97-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0e97-113">-Name</span><span class="sxs-lookup"><span data-stu-id="d0e97-113">-Name</span></span>
<span data-ttu-id="d0e97-114">Plan-Identifier-Zeichenfolge des bereitzustellenden Bilds</span><span class="sxs-lookup"><span data-stu-id="d0e97-114">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="d0e97-115">-Product</span><span class="sxs-lookup"><span data-stu-id="d0e97-115">-Product</span></span>
<span data-ttu-id="d0e97-116">Angebots Kennungszeichenfolge des bereitzustellenden Bilds.</span><span class="sxs-lookup"><span data-stu-id="d0e97-116">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="d0e97-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="d0e97-117">-Publisher</span></span>
<span data-ttu-id="d0e97-118">Herausgeber Kennungszeichenfolge des bereitzustellenden Bilds.</span><span class="sxs-lookup"><span data-stu-id="d0e97-118">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="d0e97-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0e97-119">CommonParameters</span></span>
<span data-ttu-id="d0e97-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0e97-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0e97-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0e97-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0e97-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d0e97-122">INPUTS</span></span>

### <span data-ttu-id="d0e97-123">Keine</span><span class="sxs-lookup"><span data-stu-id="d0e97-123">None</span></span>

## <span data-ttu-id="d0e97-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d0e97-124">OUTPUTS</span></span>

### <span data-ttu-id="d0e97-125">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="d0e97-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="d0e97-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="d0e97-126">NOTES</span></span>

## <span data-ttu-id="d0e97-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d0e97-127">RELATED LINKS</span></span>
