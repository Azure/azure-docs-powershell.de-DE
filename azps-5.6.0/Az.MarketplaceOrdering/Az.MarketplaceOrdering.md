---
Module Name: Az.MarketplaceOrdering
Module Guid: 6e0e216b-1dff-4992-b943-b3a4f14679ab
Download Help Link: https://docs.microsoft.com/powershell/module/az.marketplaceordering
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
ms.openlocfilehash: 2720635840051dd85eb613fabb1ac32ba32c6f60
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938624"
---
# Az.MarketplaceOrdering Module
## Beschreibung
Die Themen in diesem Abschnitt dokumentieren die Azure PowerShell-Cmdlets für Azure MarketplaceOrdering im Azure Resource Manager (ARM)-Framework. Die Cmdlets sind im Microsoft.Azure.Commands.MarketplaceOrdering-Namespace vorhanden. Diese Cmdlets ermöglichen es Azure-Benutzern, die rechtlichen Bedingungen für einen Marketplace zu akzeptieren, die eine weitere programmgesteuerte Bereitstellung für diese Lösungen ermöglichen. Benutzer können auch bereits akzeptierte gesetzliche Bestimmungen ablehnen.

## Az.MarketplaceOrdering-Cmdlets
### [Get-AzMarketplaceTerms](Get-AzMarketplaceTerms.md)
Erhalten Sie die Vertragsbedingungen für eine bestimmte Herausgeber-ID(Publisher), Angebots-ID(Produkt) und Plan-ID(Name). Das von diesem Befehl zurückgegebene Konditionenobjekt sollte an die Set-AzMarketplaceTerms übergeben werden, um die rechtlichen Bedingungen zu akzeptieren.

### [Set-AzMarketplaceTerms](Set-AzMarketplaceTerms.md)
Akzeptieren oder Ablehnen von Bedingungen für eine bestimmte Herausgeber-ID(Publisher), Angebots-ID(Produkt) und Plan-ID(Name). Verwenden Sie Get-AzMarketplaceTerms, um die Vertragsbedingungen zu erhalten.

