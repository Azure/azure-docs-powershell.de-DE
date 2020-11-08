---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/get-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: fd775b45504ec10855b54e9fd3a31d2abf8934e6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010158"
---
# <span data-ttu-id="839e1-101">Get-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="839e1-101">Get-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="839e1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="839e1-102">SYNOPSIS</span></span>
<span data-ttu-id="839e1-103">Besorgen Sie sich ein oder mehrere private Store-Angebote.</span><span class="sxs-lookup"><span data-stu-id="839e1-103">Get one or more private store's offer.</span></span>

## <span data-ttu-id="839e1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="839e1-104">SYNTAX</span></span>

```
Get-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> [-OfferId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="839e1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="839e1-105">DESCRIPTION</span></span>
<span data-ttu-id="839e1-106">Besorgen Sie sich ein oder mehrere private Store-Angebote mit öffentlich-privaten Plänen, die unter MANDANTENBEREICH hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="839e1-106">Get one or more private store's offer with public + private plans  that were added under tenant scope.</span></span> <span data-ttu-id="839e1-107">Wenn die Abonnement-ID präsentiert wird, besorgen Sie sich das Angebot eines oder mehrerer privater Stores mit privaten Plänen nur unter dem Abonnementumfang.</span><span class="sxs-lookup"><span data-stu-id="839e1-107">If subscription id is presents, get one or more private store's offer with private plans only under subscription scope</span></span>
## <span data-ttu-id="839e1-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="839e1-108">EXAMPLES</span></span>

### <span data-ttu-id="839e1-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="839e1-109">Example 1</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStoreOffer -PrivateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009182-0000-0100-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {small, medium-with-upgraded-bandwidth, medium-with-upgraded-apps, large, large-pr, small-pr}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers

UniqueOfferId             : publisherid1.offerid1
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "00009568-0000-0100-0000-5ec4f9590000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {azure_managedservices_professional ,azure_managedservices_professional-pr}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid1.offerid1
Name                      : publisherid1.offerid1
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="839e1-110">Besorgen Sie sich private Store-Angebote mit privaten + öffentlichen Plänen, die unter MANDANTENBEREICH hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="839e1-110">Get private store's offers with private + public plans  that were added under tenant scope.</span></span>

### <span data-ttu-id="839e1-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="839e1-111">Example 2</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStoreOffer -PrivateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -SubscriptionId bc17bb69-1264-4f90-a9f6-0e51e29d5281

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009182-0000-0100-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {large-pr, small-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers

UniqueOfferId             : publisherid1.offerid1
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "00009568-0000-0100-0000-5ec4f9590000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {azure_managedservices_professional-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid1.offerid1
Name                      : publisherid1.offerid1
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="839e1-112">Sie erhalten private Store-Angebote nur mit privaten Plänen, die unter Abonnementumfang hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="839e1-112">Get private store's offers with private plans only that were added under subscription scope.</span></span>

### <span data-ttu-id="839e1-113">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="839e1-113">Example 3</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStoreOffer -PrivateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -OfferId publisherid.offerid


UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009182-0000-0100-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {small, medium-with-upgraded-bandwidth, medium-with-upgraded-apps, large, large-pr, small-pr}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="839e1-114">Besorgen Sie sich das Angebot des privaten Shops mit privaten + öffentlichen Plänen, die unter MANDANTENBEREICH hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="839e1-114">Get  private store's offer with private + public plans that was been added under tenant scope.</span></span>

### <span data-ttu-id="839e1-115">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="839e1-115">Example 4</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStoreOffer -PrivateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -OfferId publisherid.offerid -SubscriptionId bc17bb69-1264-4f90-a9f6-0e51e29d5281


UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009182-0000-0100-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {large-pr, small-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="839e1-116">Sie können das Angebot des privaten Shops nur mit privaten Plänen abrufen, die unter MANDANTENBEREICH hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="839e1-116">Get private store's offer with private plans only that was been added under tenant scope.</span></span>


## <span data-ttu-id="839e1-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="839e1-117">PARAMETERS</span></span>

### <span data-ttu-id="839e1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="839e1-118">-DefaultProfile</span></span>
<span data-ttu-id="839e1-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="839e1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="839e1-120">-Angebots-Nr</span><span class="sxs-lookup"><span data-stu-id="839e1-120">-OfferId</span></span>
<span data-ttu-id="839e1-121">Erforderliches Azure Marketplace-privateStore-Angebot</span><span class="sxs-lookup"><span data-stu-id="839e1-121">Required Azure Marketplace privateStore offer</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="839e1-122">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="839e1-122">-PrivateStoreId</span></span>
<span data-ttu-id="839e1-123">Erforderliche Azure Marketplace-privateStore-Angebote</span><span class="sxs-lookup"><span data-stu-id="839e1-123">Required Azure Marketplace privateStore offers</span></span>

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

### <span data-ttu-id="839e1-124">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="839e1-124">-SubscriptionId</span></span>
<span data-ttu-id="839e1-125">Azure Marketplace-Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="839e1-125">Azure Marketplace subscription id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="839e1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="839e1-126">CommonParameters</span></span>
<span data-ttu-id="839e1-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="839e1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="839e1-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="839e1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="839e1-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="839e1-129">INPUTS</span></span>

### <span data-ttu-id="839e1-130">Keine</span><span class="sxs-lookup"><span data-stu-id="839e1-130">None</span></span>

## <span data-ttu-id="839e1-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="839e1-131">OUTPUTS</span></span>

### <span data-ttu-id="839e1-132">Microsoft. Azure. Commands. Marketplace. Models. PrivateStore. PSPrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="839e1-132">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span></span>

## <span data-ttu-id="839e1-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="839e1-133">NOTES</span></span>

## <span data-ttu-id="839e1-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="839e1-134">RELATED LINKS</span></span>
