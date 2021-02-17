---
Module Name: Az.MarketplaceOrdering
Module Guid: 6e0e216b-1dff-4992-b943-b3a4f14679ab
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
ms.openlocfilehash: dfcfd580312209bfdb0c197b95c2f655b9ac0723
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147497"
---
# <span data-ttu-id="8af84-101">Az.MarketplaceOrdering-Modul</span><span class="sxs-lookup"><span data-stu-id="8af84-101">Az.MarketplaceOrdering Module</span></span>
## <span data-ttu-id="8af84-102">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8af84-102">Description</span></span>
<span data-ttu-id="8af84-103">In den Themen in diesem Abschnitt werden die Azure -PowerShell-Cmdlets für Azure MarketplaceOrdering im Azure Resource Manager -Framework (ARM) dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="8af84-103">The topics in this section document the Azure PowerShell cmdlets for Azure MarketplaceOrdering in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="8af84-104">Die Cmdlets sind im Namespace "Microsoft.Azure.Commands.MarketplaceOrdering" vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8af84-104">The cmdlets exist in the Microsoft.Azure.Commands.MarketplaceOrdering namespace.</span></span> <span data-ttu-id="8af84-105">Diese Cmdlets ermöglichen es Azure-Benutzern, die rechtlichen Bedingungen für einen Marketplace zu akzeptieren, der eine programmgesteuerte Bereitstellung für diese Lösungen ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="8af84-105">These cmdlets allow azure users to accept the legal terms for a marketplace offering further allowing programmatic deployment for these solutions.</span></span> <span data-ttu-id="8af84-106">Benutzer können auch eine Reihe von bereits akzeptierten rechtlichen Bedingungen ablehnen.</span><span class="sxs-lookup"><span data-stu-id="8af84-106">Users may also reject set of legal terms already accepted.</span></span>

## <span data-ttu-id="8af84-107">Az.MarketplaceOrdering-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="8af84-107">Az.MarketplaceOrdering Cmdlets</span></span>
### [<span data-ttu-id="8af84-108">Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="8af84-108">Get-AzMarketplaceTerms</span></span>](Get-AzMarketplaceTerms.md)
<span data-ttu-id="8af84-109">Erhalten Sie die Vertragsbedingungen für eine bestimmte Herausgeber-ID(Publisher), Angebots-ID(Produkt) und Plan-ID(Name).</span><span class="sxs-lookup"><span data-stu-id="8af84-109">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="8af84-110">Das von diesem Befehl zurückgegebene Objekt "terms" sollte an die Set-AzMarketplaceTerms die rechtlichen Bedingungen akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="8af84-110">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

### [<span data-ttu-id="8af84-111">Set-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="8af84-111">Set-AzMarketplaceTerms</span></span>](Set-AzMarketplaceTerms.md)
<span data-ttu-id="8af84-112">Akzeptieren oder ablehnen Sie Bedingungen für eine bestimmte Herausgeber-ID(Herausgeber), Angebots-ID(Produkt) und Plan-ID(Name).</span><span class="sxs-lookup"><span data-stu-id="8af84-112">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="8af84-113">Verwenden Sie Get-AzMarketplaceTerms, um die Bedingungen des Vertrags zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8af84-113">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>

