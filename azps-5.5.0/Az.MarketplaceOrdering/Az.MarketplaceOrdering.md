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
# Az.MarketplaceOrdering-Modul
## Beschreibung
In den Themen in diesem Abschnitt werden die Azure -PowerShell-Cmdlets für Azure MarketplaceOrdering im Azure Resource Manager -Framework (ARM) dokumentiert. Die Cmdlets sind im Namespace "Microsoft.Azure.Commands.MarketplaceOrdering" vorhanden. Diese Cmdlets ermöglichen es Azure-Benutzern, die rechtlichen Bedingungen für einen Marketplace zu akzeptieren, der eine programmgesteuerte Bereitstellung für diese Lösungen ermöglicht. Benutzer können auch eine Reihe von bereits akzeptierten rechtlichen Bedingungen ablehnen.

## Az.MarketplaceOrdering-Cmdlets
### [Get-AzMarketplaceTerms](Get-AzMarketplaceTerms.md)
Erhalten Sie die Vertragsbedingungen für eine bestimmte Herausgeber-ID(Publisher), Angebots-ID(Produkt) und Plan-ID(Name). Das von diesem Befehl zurückgegebene Objekt "terms" sollte an die Set-AzMarketplaceTerms die rechtlichen Bedingungen akzeptieren.

### [Set-AzMarketplaceTerms](Set-AzMarketplaceTerms.md)
Akzeptieren oder ablehnen Sie Bedingungen für eine bestimmte Herausgeber-ID(Herausgeber), Angebots-ID(Produkt) und Plan-ID(Name). Verwenden Sie Get-AzMarketplaceTerms, um die Bedingungen des Vertrags zu erhalten.

