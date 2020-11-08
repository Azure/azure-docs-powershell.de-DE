---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/set-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Set-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Set-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: e39e3e09c99955ee90c285853988713f9a3972c4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173721"
---
# <span data-ttu-id="d58c1-101">Set-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="d58c1-101">Set-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="d58c1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d58c1-102">SYNOPSIS</span></span>
<span data-ttu-id="d58c1-103">Updates oder Angebote für den privaten Store.</span><span class="sxs-lookup"><span data-stu-id="d58c1-103">Updates or creates offer for private store.</span></span>

## <span data-ttu-id="d58c1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d58c1-104">SYNTAX</span></span>

```
Set-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> -OfferId <String>
 -SpecificPlanIdsLimitation <System.Collections.Generic.List`1[System.String]> [-ETag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d58c1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d58c1-105">DESCRIPTION</span></span>
<span data-ttu-id="d58c1-106">Aktualisiert oder erstellt ein Angebot für den privaten Speicher, das unter MANDANTENBEREICH erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d58c1-106">Updates or creates offer for private store that was created under tenant scope.</span></span>

## <span data-ttu-id="d58c1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d58c1-107">EXAMPLES</span></span>

### <span data-ttu-id="d58c1-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d58c1-108">Example 1</span></span>
```powershell
PS C:\> Set-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid -SpecificPlanIdsLimitation =@("PublisherEnterpriseLinux72", "PublisherEnterpriseLinux72-ARM", "PublisherEnterpriseLinux73", "PublisherEnterpriseLinux73-ARM ", "PublisherEnterpriseLinux73-ARM-pr")

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009562-0000-0600-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {PublisherEnterpriseLinux72, PublisherEnterpriseLinux72-ARM, PublisherEnterpriseLinux73, PublisherEnterpriseLinux73-ARM, PublisherEnterpriseLinux73-ARM-pr}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="d58c1-109">Erstellt Angebot mit privaten + öffentlichen Plänen für privaten Store, die unter MANDANTENBEREICH erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="d58c1-109">Creates offer with private + public plans for private store that was created under tenant scope.</span></span> 

### <span data-ttu-id="d58c1-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d58c1-110">Example 2</span></span>
```powershell
PS C:\> Set-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid -SubscriptionId bc17bb69-1264-4f90-a9f6-0e51e29d5281 -SpecificPlanIdsLimitation =@("PublisherEnterpriseLinux72", "PublisherEnterpriseLinux72-ARM", "PublisherEnterpriseLinux73", "PublisherEnterpriseLinux73-ARM ", "PublisherEnterpriseLinux73-ARM-pr")

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "04009562-0000-0600-0000-5ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {PublisherEnterpriseLinux73-ARM-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="d58c1-111">Erstellt Angebot mit privaten Plänen nur für privaten Store, der unter Abonnement Bereich erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d58c1-111">Creates offer with private plans only for private store that was created under subscription scope.</span></span> 

### <span data-ttu-id="d58c1-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="d58c1-112">Example 3</span></span>
```powershell
PS C:\> Set-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid -SpecificPlanIdsLimitation =@("PublisherEnterpriseLinux72", "PublisherEnterpriseLinux72-ARM", "PublisherEnterpriseLinux73") -ETag 04009562-0000-0600-0000-5ecd2fb00000

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "02009562-0000-0600-0120-3ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {PublisherEnterpriseLinux72, PublisherEnterpriseLinux72-ARM, PublisherEnterpriseLinux73}
Id                        : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="d58c1-113">Updates bieten private + öffentliche Pläne für private Stores, die unter MANDANTENBEREICH erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="d58c1-113">Updates offer with private + public plans for private store that was created under tenant scope.</span></span> <span data-ttu-id="d58c1-114">ETag wird benötigt.</span><span class="sxs-lookup"><span data-stu-id="d58c1-114">Etag is needed.</span></span>

### <span data-ttu-id="d58c1-115">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="d58c1-115">Example 4</span></span>
```powershell
PS C:\> Set-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid -SubscriptionId bc17bb69-1264-4f90-a9f6-0e51e29d5281 -SpecificPlanIdsLimitation =@("PublisherEnterpriseLinux73-pr") -ETag 04009562-0000-0600-0000-5ecd2fb00000

UniqueOfferId             : publisherid.offerid
OfferDisplayName          :
PublisherDisplayName      :
ETag                      : "02009562-0000-0600-0120-3ecd2fb00000"
PrivateStoreId            : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
CreatedBy                 :
CreatedDate               : 01/01/0001 00:00:00
SpecificPlanIdsLimitation : {PublisherEnterpriseLinux73-pr}
Id                        : /subscriptions/bc17bb69-1264-4f90-a9f6-0e51e29d5281/providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d/offers/
                            publisherid.offerid
Name                      : publisherid.offerid
Type                      : Microsoft.Marketplace/privateStores/offers
```

<span data-ttu-id="d58c1-116">Updates bieten für privaten Store nur private Pläne, die unter Abonnementumfang erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="d58c1-116">Updates offer for private store with private plans only that was created under subscription scope.</span></span> <span data-ttu-id="d58c1-117">ETag wird benötigt.</span><span class="sxs-lookup"><span data-stu-id="d58c1-117">Etag is needed.</span></span>


## <span data-ttu-id="d58c1-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="d58c1-118">PARAMETERS</span></span>

### <span data-ttu-id="d58c1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d58c1-119">-DefaultProfile</span></span>
<span data-ttu-id="d58c1-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d58c1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d58c1-121">-ETag</span><span class="sxs-lookup"><span data-stu-id="d58c1-121">-ETag</span></span>
<span data-ttu-id="d58c1-122">Azure Marketplace-privateStore-ETag-Angebot für Update</span><span class="sxs-lookup"><span data-stu-id="d58c1-122">Azure Marketplace privateStore offer's eTag for update</span></span>

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

### <span data-ttu-id="d58c1-123">-Angebots-Nr</span><span class="sxs-lookup"><span data-stu-id="d58c1-123">-OfferId</span></span>
<span data-ttu-id="d58c1-124">Erforderliches Azure Marketplace-privateStore-Angebot</span><span class="sxs-lookup"><span data-stu-id="d58c1-124">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="d58c1-125">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="d58c1-125">-PrivateStoreId</span></span>
<span data-ttu-id="d58c1-126">Erforderliche Azure Marketplace-privateStore-Angebote</span><span class="sxs-lookup"><span data-stu-id="d58c1-126">Required Azure Marketplace privateStore offers</span></span>

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

### <span data-ttu-id="d58c1-127">-SpecificPlanIdsLimitation</span><span class="sxs-lookup"><span data-stu-id="d58c1-127">-SpecificPlanIdsLimitation</span></span>
<span data-ttu-id="d58c1-128">Erforderliche Azure Marketplace-privateStore-spezifische Plan-IDs-Einschränkung</span><span class="sxs-lookup"><span data-stu-id="d58c1-128">Required Azure Marketplace privateStore offer's specific plan ids limitation</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d58c1-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d58c1-129">-Confirm</span></span>
<span data-ttu-id="d58c1-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d58c1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d58c1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d58c1-131">-WhatIf</span></span>
<span data-ttu-id="d58c1-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d58c1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d58c1-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d58c1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d58c1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d58c1-134">CommonParameters</span></span>
<span data-ttu-id="d58c1-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d58c1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d58c1-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d58c1-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d58c1-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d58c1-137">INPUTS</span></span>

### <span data-ttu-id="d58c1-138">Keine</span><span class="sxs-lookup"><span data-stu-id="d58c1-138">None</span></span>

## <span data-ttu-id="d58c1-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d58c1-139">OUTPUTS</span></span>

### <span data-ttu-id="d58c1-140">Microsoft. Azure. Commands. Marketplace. Models. PrivateStore. PSPrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="d58c1-140">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span></span>

## <span data-ttu-id="d58c1-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="d58c1-141">NOTES</span></span>

## <span data-ttu-id="d58c1-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d58c1-142">RELATED LINKS</span></span>
