---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplace/remove-azmarketplaceprivatestoreoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Remove-AzMarketplacePrivateStoreOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Remove-AzMarketplacePrivateStoreOffer.md
ms.openlocfilehash: 93c7a1e580d85201465c460740e3d6e327db22aa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154652"
---
# <span data-ttu-id="88b1e-101">Remove-AzMarketplacePrivateStoreOffer</span><span class="sxs-lookup"><span data-stu-id="88b1e-101">Remove-AzMarketplacePrivateStoreOffer</span></span>

## <span data-ttu-id="88b1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88b1e-102">SYNOPSIS</span></span>
<span data-ttu-id="88b1e-103">Entfernen sie ein Angebot aus dem privaten Store.</span><span class="sxs-lookup"><span data-stu-id="88b1e-103">Remove an offer from private store.</span></span>

## <span data-ttu-id="88b1e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="88b1e-104">SYNTAX</span></span>

```
Remove-AzMarketplacePrivateStoreOffer -PrivateStoreId <String> -OfferId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88b1e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="88b1e-105">DESCRIPTION</span></span>
<span data-ttu-id="88b1e-106">Entfernen Sie ein Angebot aus einem privaten Store, das im Mandantenbereich erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="88b1e-106">Remove an offer from private store that was created in tenant scope.</span></span>

## <span data-ttu-id="88b1e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="88b1e-107">EXAMPLES</span></span>

### <span data-ttu-id="88b1e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="88b1e-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzMarketplacePrivateStoreOffer -privateStoreId 7gh67884-1r56-44fb-a93d-030d4ae08b2d -offerId  publisherid.offerid
```

<span data-ttu-id="88b1e-109">Entfernen Sie ein Angebot aus einem privaten Store, das im Mandantenbereich erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="88b1e-109">Remove an offer from private store that was created in tenant scope.</span></span>

## <span data-ttu-id="88b1e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88b1e-110">PARAMETERS</span></span>

### <span data-ttu-id="88b1e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88b1e-111">-DefaultProfile</span></span>
<span data-ttu-id="88b1e-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="88b1e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88b1e-113">-OfferId</span><span class="sxs-lookup"><span data-stu-id="88b1e-113">-OfferId</span></span>
<span data-ttu-id="88b1e-114">Erforderliches Azure Marketplace privateStore-Angebot</span><span class="sxs-lookup"><span data-stu-id="88b1e-114">Required Azure Marketplace privateStore offer</span></span>

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

### <span data-ttu-id="88b1e-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="88b1e-115">-PassThru</span></span>
<span data-ttu-id="88b1e-116">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="88b1e-116">{{ Fill PassThru Description }}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88b1e-117">-PrivateStoreId</span><span class="sxs-lookup"><span data-stu-id="88b1e-117">-PrivateStoreId</span></span>
<span data-ttu-id="88b1e-118">Erforderlicher Azure Marketplace privateStore</span><span class="sxs-lookup"><span data-stu-id="88b1e-118">Required Azure Marketplace privateStore</span></span>

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

### <span data-ttu-id="88b1e-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="88b1e-119">-Confirm</span></span>
<span data-ttu-id="88b1e-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="88b1e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88b1e-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="88b1e-121">-WhatIf</span></span>
<span data-ttu-id="88b1e-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="88b1e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88b1e-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="88b1e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88b1e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88b1e-124">CommonParameters</span></span>
<span data-ttu-id="88b1e-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88b1e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88b1e-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="88b1e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88b1e-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="88b1e-127">INPUTS</span></span>

### <span data-ttu-id="88b1e-128">Keine</span><span class="sxs-lookup"><span data-stu-id="88b1e-128">None</span></span>

## <span data-ttu-id="88b1e-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="88b1e-129">OUTPUTS</span></span>

### <span data-ttu-id="88b1e-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="88b1e-130">System.Boolean</span></span>

## <span data-ttu-id="88b1e-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="88b1e-131">NOTES</span></span>

## <span data-ttu-id="88b1e-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="88b1e-132">RELATED LINKS</span></span>
