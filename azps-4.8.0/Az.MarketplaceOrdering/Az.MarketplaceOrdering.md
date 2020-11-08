---
Module Name: Az.MarketplaceOrdering
Module Guid: 6e0e216b-1dff-4992-b943-b3a4f14679ab
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
ms.openlocfilehash: dfcfd580312209bfdb0c197b95c2f655b9ac0723
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173722"
---
# <span data-ttu-id="28d96-101">AZ. MarketplaceOrdering-Modul</span><span class="sxs-lookup"><span data-stu-id="28d96-101">Az.MarketplaceOrdering Module</span></span>
## <span data-ttu-id="28d96-102">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="28d96-102">Description</span></span>
<span data-ttu-id="28d96-103">In den Themen in diesem Abschnitt werden die Azure PowerShell-Cmdlets für Azure MarketplaceOrdering im Azure Resource Manager (Arm)-Framework dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="28d96-103">The topics in this section document the Azure PowerShell cmdlets for Azure MarketplaceOrdering in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="28d96-104">Die Cmdlets sind im Microsoft. Azure. Commands. MarketplaceOrdering-Namespace vorhanden.</span><span class="sxs-lookup"><span data-stu-id="28d96-104">The cmdlets exist in the Microsoft.Azure.Commands.MarketplaceOrdering namespace.</span></span> <span data-ttu-id="28d96-105">Mit diesen Cmdlets können Azure-Benutzer die rechtlichen Best imbegriffe für einen Marktplatz akzeptieren, der die programmgesteuerte Bereitstellung für diese Lösungen weiter ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="28d96-105">These cmdlets allow azure users to accept the legal terms for a marketplace offering further allowing programmatic deployment for these solutions.</span></span> <span data-ttu-id="28d96-106">Benutzer können auch eine Reihe rechtlicher Best imbegriffe ablehnen, die bereits akzeptiert wurden.</span><span class="sxs-lookup"><span data-stu-id="28d96-106">Users may also reject set of legal terms already accepted.</span></span>

## <span data-ttu-id="28d96-107">AZ. MarketplaceOrdering-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="28d96-107">Az.MarketplaceOrdering Cmdlets</span></span>
### [<span data-ttu-id="28d96-108">Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="28d96-108">Get-AzMarketplaceTerms</span></span>](Get-AzMarketplaceTerms.md)
<span data-ttu-id="28d96-109">Besorgen Sie sich die Vertragsbedingungen für eine bestimmte Publisher-ID (Publisher), Angebots-ID (Produkt) und Plan-ID (Name).</span><span class="sxs-lookup"><span data-stu-id="28d96-109">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="28d96-110">Die von diesem Befehl zurückgegebenen Ausdrücke-Objekte sollten an Set-AzMarketplaceTerms übergeben werden, um die rechtlichen Best imbegriffe zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="28d96-110">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

### [<span data-ttu-id="28d96-111">Satz-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="28d96-111">Set-AzMarketplaceTerms</span></span>](Set-AzMarketplaceTerms.md)
<span data-ttu-id="28d96-112">Akzeptieren oder ablehnen von Ausdrücken für eine bestimmte Publisher-ID (Publisher), Angebots-ID (Produkt) und Plan-ID (Name).</span><span class="sxs-lookup"><span data-stu-id="28d96-112">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="28d96-113">Bitte verwenden Sie Get-AzMarketplaceTerms, um die Vertragsbedingungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="28d96-113">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>

