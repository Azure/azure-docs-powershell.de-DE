---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/new-azurermanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallRule.md
ms.openlocfilehash: 74a6d563772e84c7356c400b674cbab960ee8dd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500649"
---
# <span data-ttu-id="9d948-101">New-AzureRmAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9d948-101">New-AzureRmAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="9d948-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9d948-102">SYNOPSIS</span></span>
<span data-ttu-id="9d948-103">Erstellt eine neue Analysis Services-Firewallregel</span><span class="sxs-lookup"><span data-stu-id="9d948-103">Creates a new Analysis Services firewall rule</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d948-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d948-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String> [-RangeEnd] <String>
```

## <span data-ttu-id="9d948-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9d948-105">DESCRIPTION</span></span>
<span data-ttu-id="9d948-106">Das New-AzureRmAnalysisServicesFirewallRule erstellt ein neues Firewallregel-Objekt.</span><span class="sxs-lookup"><span data-stu-id="9d948-106">The New-AzureRmAnalysisServicesFirewallRule creates a new firewall rule object.</span></span>

## <span data-ttu-id="9d948-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9d948-107">EXAMPLES</span></span>

### <span data-ttu-id="9d948-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9d948-108">Example 1</span></span>
```
PS C:\> New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

<span data-ttu-id="9d948-109">Erstellt eine Firewallregel mit dem Namen "rule1" mit dem Anfangsbereich 0.0.0.0 und dem Endbereich 255.255.255.255</span><span class="sxs-lookup"><span data-stu-id="9d948-109">Creates a firewall rule named rule1 with start range 0.0.0.0 and end range 255.255.255.255</span></span>

## <span data-ttu-id="9d948-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d948-110">PARAMETERS</span></span>

### <span data-ttu-id="9d948-111">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="9d948-111">-FirewallRuleName</span></span>
<span data-ttu-id="9d948-112">Name der Firewall-Regel</span><span class="sxs-lookup"><span data-stu-id="9d948-112">Name of firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d948-113">-RangeStart</span><span class="sxs-lookup"><span data-stu-id="9d948-113">-RangeStart</span></span>
<span data-ttu-id="9d948-114">Der Bereichsanfang einer Firewallregel</span><span class="sxs-lookup"><span data-stu-id="9d948-114">The range start of a firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d948-115">-RangeEnd</span><span class="sxs-lookup"><span data-stu-id="9d948-115">-RangeEnd</span></span>
<span data-ttu-id="9d948-116">Das Bereichsende einer Firewallregel</span><span class="sxs-lookup"><span data-stu-id="9d948-116">The range end of a firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="9d948-117">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9d948-117">INPUTS</span></span>

## <span data-ttu-id="9d948-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9d948-118">OUTPUTS</span></span>

### <span data-ttu-id="9d948-119">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9d948-119">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="9d948-120">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9d948-120">RELATED LINKS</span></span>

[<span data-ttu-id="9d948-121">Neu – AzureRmAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="9d948-121">New-AzureRmAnalysisServicesFirewallConfig</span></span>](./New-AzureRmAnalysisServicesFirewallConfig.md)
