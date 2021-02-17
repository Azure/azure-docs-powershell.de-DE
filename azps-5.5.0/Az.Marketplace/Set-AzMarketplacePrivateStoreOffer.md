---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/set-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Set-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Set-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: e39e3e09c99955ee90c285853988713f9a3972c4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147505"
---
# <span data-ttu-id="08cd3-101">Set-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="08cd3-101">Set-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="08cd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08cd3-102">SYNOPSIS</span></span>
<span data-ttu-id="08cd3-103">Aktualisiert oder erstellt ein Angebot für einen privaten Store.</span><span class="sxs-lookup"><span data-stu-id="08cd3-103">Updates or creates offer for private store.</span></span>

## <span data-ttu-id="08cd3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="08cd3-104">SYNTAX</span></span>

```
Set-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> -OfferId <String>
 -SpecificPlanIdsLimitation <System.Collections.Generic.List`1[System.String]> [-ETag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08cd3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="08cd3-105">DESCRIPTION</span></span>
<span data-ttu-id="08cd3-106">Aktualisiert oder erstellt ein Angebot für einen privaten Store, das im Mandantenbereich erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="08cd3-106">Updates or creates offer for private store that was created under tenant scope.</span></span>

## <span data-ttu-id="08cd3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="08cd3-107">EXAMPLES</span></span>

### <span data-ttu-id="08cd3-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="08cd3-108">Example 1</span></span>
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

<span data-ttu-id="08cd3-109">Erstellt ein Angebot mit privaten und öffentlichen Plänen für einen privaten Store, das im Mandantenbereich erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="08cd3-109">Creates offer with private + public plans for private store that was created under tenant scope.</span></span> 

### <span data-ttu-id="08cd3-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="08cd3-110">Example 2</span></span>
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

<span data-ttu-id="08cd3-111">Erstellt ein Angebot mit privaten Plänen nur für einen privaten Store, der im Abonnementbereich erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="08cd3-111">Creates offer with private plans only for private store that was created under subscription scope.</span></span> 

### <span data-ttu-id="08cd3-112">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="08cd3-112">Example 3</span></span>
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

<span data-ttu-id="08cd3-113">Aktualisierungsangebot mit privaten und öffentlichen Plänen für privaten Store, die im Mandantenbereich erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="08cd3-113">Updates offer with private + public plans for private store that was created under tenant scope.</span></span> <span data-ttu-id="08cd3-114">Ein Etag ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="08cd3-114">Etag is needed.</span></span>

### <span data-ttu-id="08cd3-115">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="08cd3-115">Example 4</span></span>
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

<span data-ttu-id="08cd3-116">Aktualisierungsangebot für privaten Store mit privaten Plänen, die nur im Rahmen des Abonnementumfangs erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="08cd3-116">Updates offer for private store with private plans only that was created under subscription scope.</span></span> <span data-ttu-id="08cd3-117">Ein Etag ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="08cd3-117">Etag is needed.</span></span>


## <span data-ttu-id="08cd3-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08cd3-118">PARAMETERS</span></span>

### <span data-ttu-id="08cd3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08cd3-119">-DefaultProfile</span></span>
<span data-ttu-id="08cd3-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="08cd3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08cd3-121">-ETag</span><span class="sxs-lookup"><span data-stu-id="08cd3-121">-ETag</span></span>
<span data-ttu-id="08cd3-122">eTag für das Update des Azure Marketplace-PrivateStore-Angebots</span><span class="sxs-lookup"><span data-stu-id="08cd3-122">Azure Marketplace privateStore offer's eTag for update</span></span>

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

### <span data-ttu-id="08cd3-123">-OfferId</span><span class="sxs-lookup"><span data-stu-id="08cd3-123">-OfferId</span></span>
<span data-ttu-id="08cd3-124">Erforderliches Azure Marketplace privateStore-Angebot</span><span class="sxs-lookup"><span data-stu-id="08cd3-124">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="08cd3-125">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="08cd3-125">-PrivateStoreId</span></span>
<span data-ttu-id="08cd3-126">Erforderliche Angebote von Azure Marketplace privateStore</span><span class="sxs-lookup"><span data-stu-id="08cd3-126">Required Azure Marketplace privateStore offers</span></span>

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

### <span data-ttu-id="08cd3-127">-SpecificPlanIdsLimitation</span><span class="sxs-lookup"><span data-stu-id="08cd3-127">-SpecificPlanIdsLimitation</span></span>
<span data-ttu-id="08cd3-128">Spezifische Einschränkung der Plan-IDs des erforderlichen Azure Marketplace privateStore-Angebots</span><span class="sxs-lookup"><span data-stu-id="08cd3-128">Required Azure Marketplace privateStore offer's specific plan ids limitation</span></span>

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

### <span data-ttu-id="08cd3-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="08cd3-129">-Confirm</span></span>
<span data-ttu-id="08cd3-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="08cd3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08cd3-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="08cd3-131">-WhatIf</span></span>
<span data-ttu-id="08cd3-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="08cd3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08cd3-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="08cd3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08cd3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08cd3-134">CommonParameters</span></span>
<span data-ttu-id="08cd3-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08cd3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08cd3-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="08cd3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08cd3-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="08cd3-137">INPUTS</span></span>

### <span data-ttu-id="08cd3-138">Keine</span><span class="sxs-lookup"><span data-stu-id="08cd3-138">None</span></span>

## <span data-ttu-id="08cd3-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="08cd3-139">OUTPUTS</span></span>

### <span data-ttu-id="08cd3-140">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="08cd3-140">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStoreOffer</span></span>

## <span data-ttu-id="08cd3-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="08cd3-141">NOTES</span></span>

## <span data-ttu-id="08cd3-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="08cd3-142">RELATED LINKS</span></span>
