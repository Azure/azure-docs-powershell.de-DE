---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Marketplace.dll-Help.xml
Module Name: Az.Marketplace
online version: https://docs.microsoft.com/powershell/module/az.marketplace/get-azmarketplaceprivatestore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Marketplace/Marketplace/help/Get-AzMarketplacePrivateStore.md
ms.openlocfilehash: 2dd2ec778a64403b9f13cd923e7b7312e72a6c84
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945016"
---
# <span data-ttu-id="5470d-101">Get-AzMarketplacePrivateStore</span><span class="sxs-lookup"><span data-stu-id="5470d-101">Get-AzMarketplacePrivateStore</span></span>

## <span data-ttu-id="5470d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5470d-102">SYNOPSIS</span></span>
<span data-ttu-id="5470d-103">Liste des privaten Speichers herunterladen</span><span class="sxs-lookup"><span data-stu-id="5470d-103">Get private store list</span></span>

## <span data-ttu-id="5470d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5470d-104">SYNTAX</span></span>

```
Get-AzMarketplacePrivateStore [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5470d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5470d-105">DESCRIPTION</span></span>
<span data-ttu-id="5470d-106">Private Store-Liste herunterladen, die im Mandantenbereich erstellt wurden</span><span class="sxs-lookup"><span data-stu-id="5470d-106">Get private store list that were created under tenant scope</span></span>

## <span data-ttu-id="5470d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5470d-107">EXAMPLES</span></span>

### <span data-ttu-id="5470d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5470d-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMarketplacePrivateStore


Availability   : enabled
PrivateStoreId : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
ETag           : "47006253-0000-0100-0000-5ecb6df90000"
Id             : /providers/Microsoft.Marketplace/privateStores/7gh67884-1r56-44fb-a93d-030d4ae08b2d
Name           : 7gh67884-1r56-44fb-a93d-030d4ae08b2d
Type           : Microsoft.Marketplace/privateStores
```

<span data-ttu-id="5470d-109">Private Store-Liste, die im Mandantenbereich erstellt wurde</span><span class="sxs-lookup"><span data-stu-id="5470d-109">private store list that were created under tenant scope</span></span>

## <span data-ttu-id="5470d-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5470d-110">PARAMETERS</span></span>

### <span data-ttu-id="5470d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5470d-111">-DefaultProfile</span></span>
<span data-ttu-id="5470d-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5470d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5470d-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5470d-113">CommonParameters</span></span>
<span data-ttu-id="5470d-114">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5470d-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5470d-115">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5470d-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5470d-116">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5470d-116">INPUTS</span></span>

### <span data-ttu-id="5470d-117">Keine</span><span class="sxs-lookup"><span data-stu-id="5470d-117">None</span></span>

## <span data-ttu-id="5470d-118">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5470d-118">OUTPUTS</span></span>

### <span data-ttu-id="5470d-119">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStore</span><span class="sxs-lookup"><span data-stu-id="5470d-119">Microsoft.Azure.Commands.Marketplace.Models.PrivateStore.PSPrivateStore</span></span>

## <span data-ttu-id="5470d-120">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5470d-120">NOTES</span></span>

## <span data-ttu-id="5470d-121">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5470d-121">RELATED LINKS</span></span>
