---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrulegroupoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
ms.openlocfilehash: 81b09a392464a004030a0798ea211db08a60a9f4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98302187"
---
# <span data-ttu-id="f7662-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="f7662-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="f7662-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7662-102">SYNOPSIS</span></span>
<span data-ttu-id="f7662-103">Erstellt den Eintrag "RuleGroupOverride" in "ManagedRuleSets" für die Firewallrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="f7662-103">Creates RuleGroupOverride entry in ManagedRuleSets for the firewall policy.</span></span>

## <span data-ttu-id="f7662-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f7662-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName <String>
 -Rule <PSApplicationGatewayFirewallPolicyManagedRuleOverride[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f7662-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f7662-105">DESCRIPTION</span></span>
<span data-ttu-id="f7662-106">Die **Neue-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** erstellt einen Regeleintrag "GroupOverride" in einem managedRuleSet für eine Firewallrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="f7662-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** creates a ruleGroupOverride entry in a managedRuleSet for a firewall policy.</span></span>

## <span data-ttu-id="f7662-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f7662-107">EXAMPLES</span></span>

### <span data-ttu-id="f7662-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f7662-108">Example 1</span></span>
```powershell
PS C:\> $overrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName $ruleName -Rules $rule1,$rule2
```

<span data-ttu-id="f7662-109">Erstellt einen Eintrag "RuleGroupOverride" mit dem Gruppennamen $ruleName und Regeln als $rule 1, $rule 2.</span><span class="sxs-lookup"><span data-stu-id="f7662-109">Creates a RuleGroupOverride entry with group name as $ruleName and Rules as $rule1, $rule2.</span></span> <span data-ttu-id="f7662-110">Weist die gleiche Zuordnung zu $overrideEntry</span><span class="sxs-lookup"><span data-stu-id="f7662-110">Assigns the same to $overrideEntry</span></span>

## <span data-ttu-id="f7662-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7662-111">PARAMETERS</span></span>

### <span data-ttu-id="f7662-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7662-112">-DefaultProfile</span></span>
<span data-ttu-id="f7662-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f7662-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7662-114">-Rule</span><span class="sxs-lookup"><span data-stu-id="f7662-114">-Rule</span></span>
<span data-ttu-id="f7662-115">Liste der Regeln.</span><span class="sxs-lookup"><span data-stu-id="f7662-115">List of Rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7662-116">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="f7662-116">-RuleGroupName</span></span>
<span data-ttu-id="f7662-117">Geben Sie den Regelgruppennamen in einem Eintrag zur Außerkraftsetzung der Regelgruppe an.</span><span class="sxs-lookup"><span data-stu-id="f7662-117">Specify the ruleGroupName in a override RuleGroup entry.</span></span>

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

### <span data-ttu-id="f7662-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7662-118">CommonParameters</span></span>
<span data-ttu-id="f7662-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7662-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7662-120">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7662-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7662-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f7662-121">INPUTS</span></span>

### <span data-ttu-id="f7662-122">Keine</span><span class="sxs-lookup"><span data-stu-id="f7662-122">None</span></span>

## <span data-ttu-id="f7662-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f7662-123">OUTPUTS</span></span>

### <span data-ttu-id="f7662-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="f7662-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="f7662-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f7662-125">NOTES</span></span>

## <span data-ttu-id="f7662-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f7662-126">RELATED LINKS</span></span>
