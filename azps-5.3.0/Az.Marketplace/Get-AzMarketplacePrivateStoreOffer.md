---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/get-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: fd775b45504ec10855b54e9fd3a31d2abf8934e6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467603"
---
# <span data-ttu-id="a39de-101">Get-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="a39de-101">Get-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="a39de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a39de-102">SYNOPSIS</span></span>
<span data-ttu-id="a39de-103">Holen Sie sich das Angebot eines privaten Store.</span><span class="sxs-lookup"><span data-stu-id="a39de-103">Get one or more private store's offer.</span></span>

## <span data-ttu-id="a39de-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a39de-104">SYNTAX</span></span>

```
Get-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> [-OfferId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a39de-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a39de-105">DESCRIPTION</span></span>
<span data-ttu-id="a39de-106">Holen Sie sich das Angebot eines privaten Store mit öffentlichen und privaten Plänen, die im Mandantenbereich hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="a39de-106">Get one or more private store's offer with public + private plans  that were added under tenant scope.</span></span> <span data-ttu-id="a39de-107">Wenn eine Abonnement-ID angezeigt wird, erhalten Sie das Angebot eines privaten Store mit privaten Plänen nur im Rahmen des Abonnementumfangs.</span><span class="sxs-lookup"><span data-stu-id="a39de-107">If subscription id is presents, get one or more private store's offer with private plans only under subscription scope</span></span>
## <span data-ttu-id="a39de-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a39de-108">EXAMPLES</span></span>

### <span data-ttu-id="a39de-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a39de-109">Example 1</span></span>
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

<span data-ttu-id="a39de-110">Holen Sie sich Angebote privater Store mit privaten und öffentlichen Plänen, die im Mandantenbereich hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="a39de-110">Get private store's offers with private + public plans  that were added under tenant scope.</span></span>

### <span data-ttu-id="a39de-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a39de-111">Example 2</span></span>
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

<span data-ttu-id="a39de-112">Erhalten Sie Angebote privater Store nur mit privaten Plänen, die im Abonnementbereich hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="a39de-112">Get private store's offers with private plans only that were added under subscription scope.</span></span>

### <span data-ttu-id="a39de-113">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="a39de-113">Example 3</span></span>
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

<span data-ttu-id="a39de-114">Holen Sie sich das Angebot eines privaten Store mit privaten und öffentlichen Plänen, die im Mandantenbereich hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="a39de-114">Get  private store's offer with private + public plans that was been added under tenant scope.</span></span>

### <span data-ttu-id="a39de-115">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="a39de-115">Example 4</span></span>
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

<span data-ttu-id="a39de-116">Holen Sie sich das Angebot eines privaten Store nur mit privaten Plänen, die im Mandantenbereich hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="a39de-116">Get private store's offer with private plans only that was been added under tenant scope.</span></span>


## <span data-ttu-id="a39de-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a39de-117">PARAMETERS</span></span>

### <span data-ttu-id="a39de-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a39de-118">-DefaultProfile</span></span>
<span data-ttu-id="a39de-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a39de-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a39de-120">-OfferId</span><span class="sxs-lookup"><span data-stu-id="a39de-120">-OfferId</span></span>
<span data-ttu-id="a39de-121">Erforderliches Azure Marketplace privateStore-Angebot</span><span class="sxs-lookup"><span data-stu-id="a39de-121">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="a39de-122">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="a39de-122">-PrivateStoreId</span></span>
<span data-ttu-id="a39de-123">Erforderliche Angebote von Azure Marketplace privateStore</span><span class="sxs-lookup"><span data-stu-id="a39de-123">Required Azure Marketplace privateStore offers</span></span>

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

### <span data-ttu-id="a39de-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a39de-124">-SubscriptionId</span></span>
<span data-ttu-id="a39de-125">Azure Marketplace-Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="a39de-125">Azure Marketplace subscription id</span></span>

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

### <span data-ttu-id="a39de-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a39de-126">CommonParameters</span></span>
<span data-ttu-id="a39de-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a39de-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a39de-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a39de-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a39de-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a39de-129">INPUTS</span></span>

### <span data-ttu-id="a39de-130">Keine</span><span class="sxs-lookup"><span data-stu-id="a39de-130">None</span></span>

## <span data-ttu-id="a39de-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a39de-131">OUTPUTS</span></span>

### <span data-ttu-id="a39de-132">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="a39de-132">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span></span>

## <span data-ttu-id="a39de-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a39de-133">NOTES</span></span>

## <span data-ttu-id="a39de-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a39de-134">RELATED LINKS</span></span>
