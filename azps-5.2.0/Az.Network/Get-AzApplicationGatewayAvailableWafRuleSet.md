---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablewafruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
ms.openlocfilehash: 7cb3f6d015f95ba6a72066714647eb7a0551398b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98307187"
---
# <span data-ttu-id="f0dc3-101">Get-AzApplicationGatewayAvailableWafRuleSet</span><span class="sxs-lookup"><span data-stu-id="f0dc3-101">Get-AzApplicationGatewayAvailableWafRuleSet</span></span>

## <span data-ttu-id="f0dc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0dc3-102">SYNOPSIS</span></span>
<span data-ttu-id="f0dc3-103">Ruft alle verfügbaren Firewallregelsätze für Webanwendungen ab.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-103">Gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="f0dc3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f0dc3-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableWafRuleSet [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0dc3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f0dc3-105">DESCRIPTION</span></span>
<span data-ttu-id="f0dc3-106">Das **Cmdlet "Get-AzApplicationGatewayAvailableWafRuleSet"** ruft alle verfügbaren Firewallregelsätze für Webanwendungen ab.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-106">The **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="f0dc3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f0dc3-107">EXAMPLES</span></span>

### <span data-ttu-id="f0dc3-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f0dc3-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzApplicationGatewayAvailableWafRuleSet
```

<span data-ttu-id="f0dc3-109">Diese Befehle geben alle verfügbaren Firewallregelsätze für Webanwendungen zurück.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="f0dc3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0dc3-110">PARAMETERS</span></span>

### <span data-ttu-id="f0dc3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0dc3-111">-DefaultProfile</span></span>
<span data-ttu-id="f0dc3-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0dc3-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0dc3-113">CommonParameters</span></span>
<span data-ttu-id="f0dc3-114">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0dc3-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0dc3-115">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f0dc3-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0dc3-116">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f0dc3-116">INPUTS</span></span>

### <span data-ttu-id="f0dc3-117">Keine</span><span class="sxs-lookup"><span data-stu-id="f0dc3-117">None</span></span>

## <span data-ttu-id="f0dc3-118">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f0dc3-118">OUTPUTS</span></span>

### <span data-ttu-id="f0dc3-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="f0dc3-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="f0dc3-120">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f0dc3-120">NOTES</span></span>
<span data-ttu-id="f0dc3-121">**List-AzApplicationGatewayAvailableWafRuleSets** ist ein Alias für das **Cmdlet "Get-AzApplicationGatewayAvailableWafRuleSet".**</span><span class="sxs-lookup"><span data-stu-id="f0dc3-121">**List-AzApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet.</span></span>

## <span data-ttu-id="f0dc3-122">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f0dc3-122">RELATED LINKS</span></span>
