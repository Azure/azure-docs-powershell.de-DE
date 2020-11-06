---
Module Name: AzureRM.MarketplaceOrdering
Module Guid: 6e0e216b-1dff-4992-b943-b3a4f14679ab
Download Help Link: ''
Help Version: 0.1.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/AzureRM.MarketplaceOrdering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/AzureRM.MarketplaceOrdering.md
ms.openlocfilehash: f1446494d4eb68195ec0cefba248f519039a91ce
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "93474014"
---
# <span data-ttu-id="c98fc-101">AzureRM. MarketplaceOrdering-Modul</span><span class="sxs-lookup"><span data-stu-id="c98fc-101">AzureRM.MarketplaceOrdering Module</span></span>
## <span data-ttu-id="c98fc-102">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c98fc-102">Description</span></span>
<span data-ttu-id="c98fc-103">In den Themen in diesem Abschnitt werden die Azure PowerShell-Cmdlets für Azure MarketplaceOrdering im Azure Resource Manager (Arm)-Framework dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="c98fc-103">The topics in this section document the Azure PowerShell cmdlets for Azure MarketplaceOrdering in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="c98fc-104">Die Cmdlets sind im Microsoft. Azure. Commands. MarketplaceOrdering-Namespace vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c98fc-104">The cmdlets exist in the Microsoft.Azure.Commands.MarketplaceOrdering namespace.</span></span> <span data-ttu-id="c98fc-105">Mithilfe dieser Cmdlets können Azure-Benutzer die Rechtsbegriffe für einen Marktplatz akzeptieren, der die programmtic-Bereitstellung für diese Lösungen weiter ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="c98fc-105">These cmdlets allow azure users to accept the legal terms for a marketplace offering further allowing programmtic deployment for these solutions.</span></span> <span data-ttu-id="c98fc-106">Benutzer können auch eine Reihe rechtlicher Best imbegriffe ablehnen, die bereits akzeptiert wurden.</span><span class="sxs-lookup"><span data-stu-id="c98fc-106">Users may also reject set of legal terms already accepted.</span></span>

## <span data-ttu-id="c98fc-107">AzureRM. MarketplaceOrdering-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="c98fc-107">AzureRM.MarketplaceOrdering Cmdlets</span></span>
### [<span data-ttu-id="c98fc-108">Get-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="c98fc-108">Get-AzureRmMarketplaceTerms</span></span>](Get-AzureRmMarketplaceTerms.md)
<span data-ttu-id="c98fc-109">Besorgen Sie sich die Vertragsbedingungen für eine bestimmte Publisher-ID (Publisher), Angebots-ID (Produkt) und Plan-ID (Name).</span><span class="sxs-lookup"><span data-stu-id="c98fc-109">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="c98fc-110">Die von diesem Befehl zurückgegebenen Ausdrücke-Objekte sollten an Set-AzureRmMarketplaceTerms übergeben werden, um die rechtlichen Best imbegriffe zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="c98fc-110">The terms object which is returned by this command should be passed to Set-AzureRmMarketplaceTerms to accept the legal terms.</span></span>

### [<span data-ttu-id="c98fc-111">Satz-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="c98fc-111">Set-AzureRmMarketplaceTerms</span></span>](Set-AzureRmMarketplaceTerms.md)
<span data-ttu-id="c98fc-112">Akzeptieren oder ablehnen der Rechtsbegriffe für eine bestimmte Publisher-ID (Publisher), Angebots-ID (Produkt) und Plan-ID (Name).</span><span class="sxs-lookup"><span data-stu-id="c98fc-112">Accept or reject the legal terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="c98fc-113">Bitte verwenden Sie Get-AzureRmMarketplaceTerms, um die Vertragsbedingungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c98fc-113">Please use Get-AzureRmMarketplaceTerms to get the agreement terms.</span></span>

