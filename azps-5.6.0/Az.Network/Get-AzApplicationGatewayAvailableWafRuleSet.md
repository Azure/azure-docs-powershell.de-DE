---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayavailablewafruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableWafRuleSet.md
ms.openlocfilehash: b914e87729e97bb6b8af9ec59605290e0cc025bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931795"
---
# <span data-ttu-id="402fa-101">Get-AzApplicationGatewayAvailableWafRuleSet</span><span class="sxs-lookup"><span data-stu-id="402fa-101">Get-AzApplicationGatewayAvailableWafRuleSet</span></span>

## <span data-ttu-id="402fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="402fa-102">SYNOPSIS</span></span>
<span data-ttu-id="402fa-103">Ruft alle verfügbaren Firewallregelsätze für Webanwendungen ab.</span><span class="sxs-lookup"><span data-stu-id="402fa-103">Gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="402fa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="402fa-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableWafRuleSet [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="402fa-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="402fa-105">DESCRIPTION</span></span>
<span data-ttu-id="402fa-106">Das **Get-AzApplicationGatewayAvailableWafRuleSet-Cmdlet** ruft alle verfügbaren Firewallregelsätze für Webanwendungen ab.</span><span class="sxs-lookup"><span data-stu-id="402fa-106">The **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet gets all available web application firewall rule sets.</span></span>

## <span data-ttu-id="402fa-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="402fa-107">EXAMPLES</span></span>

### <span data-ttu-id="402fa-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="402fa-108">Example 1</span></span>
```
PS C:\>$availableRuleSets = Get-AzApplicationGatewayAvailableWafRuleSet
```

<span data-ttu-id="402fa-109">Mit diesen Befehlen werden alle verfügbaren Firewallregelsätze für Webanwendungen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="402fa-109">This commands returns all the available web application firewall rule sets.</span></span>

## <span data-ttu-id="402fa-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="402fa-110">PARAMETERS</span></span>

### <span data-ttu-id="402fa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="402fa-111">-DefaultProfile</span></span>
<span data-ttu-id="402fa-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="402fa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="402fa-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="402fa-113">CommonParameters</span></span>
<span data-ttu-id="402fa-114">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="402fa-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="402fa-115">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="402fa-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="402fa-116">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="402fa-116">INPUTS</span></span>

### <span data-ttu-id="402fa-117">Keine</span><span class="sxs-lookup"><span data-stu-id="402fa-117">None</span></span>

## <span data-ttu-id="402fa-118">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="402fa-118">OUTPUTS</span></span>

### <span data-ttu-id="402fa-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span><span class="sxs-lookup"><span data-stu-id="402fa-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableWafRuleSetsResult</span></span>

## <span data-ttu-id="402fa-120">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="402fa-120">NOTES</span></span>
<span data-ttu-id="402fa-121">**List-AzApplicationGatewayAvailableWafRuleSets** ist ein Alias für das **Get-AzApplicationGatewayAvailableWafRuleSet-Cmdlet.**</span><span class="sxs-lookup"><span data-stu-id="402fa-121">**List-AzApplicationGatewayAvailableWafRuleSets** is an alias for the **Get-AzApplicationGatewayAvailableWafRuleSet** cmdlet.</span></span>

## <span data-ttu-id="402fa-122">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="402fa-122">RELATED LINKS</span></span>
