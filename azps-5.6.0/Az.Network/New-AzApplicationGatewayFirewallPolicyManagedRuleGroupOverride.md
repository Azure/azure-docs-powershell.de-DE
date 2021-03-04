---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrulegroupoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
ms.openlocfilehash: 6b105ab242f9ffb64d1d523cad5930c48714c724
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944021"
---
# <span data-ttu-id="06d64-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="06d64-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="06d64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06d64-102">SYNOPSIS</span></span>
<span data-ttu-id="06d64-103">Erstellt den Eintrag RuleGroupOverride in ManagedRuleSets für die Firewallrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="06d64-103">Creates RuleGroupOverride entry in ManagedRuleSets for the firewall policy.</span></span>

## <span data-ttu-id="06d64-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="06d64-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName <String>
 -Rule <PSApplicationGatewayFirewallPolicyManagedRuleOverride[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="06d64-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="06d64-105">DESCRIPTION</span></span>
<span data-ttu-id="06d64-106">Die **New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** erstellt einen RegelGroupOverride-Eintrag in einem managedRuleSet für eine Firewallrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="06d64-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** creates a ruleGroupOverride entry in a managedRuleSet for a firewall policy.</span></span>

## <span data-ttu-id="06d64-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="06d64-107">EXAMPLES</span></span>

### <span data-ttu-id="06d64-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="06d64-108">Example 1</span></span>
```powershell
PS C:\> $overrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName $ruleName -Rules $rule1,$rule2
```

<span data-ttu-id="06d64-109">Erstellt einen Eintrag RuleGroupOverride mit dem Gruppennamen als $ruleName und Regeln als $rule 1, $rule 2.</span><span class="sxs-lookup"><span data-stu-id="06d64-109">Creates a RuleGroupOverride entry with group name as $ruleName and Rules as $rule1, $rule2.</span></span> <span data-ttu-id="06d64-110">Weist dem Benutzer dasselbe $overrideEntry</span><span class="sxs-lookup"><span data-stu-id="06d64-110">Assigns the same to $overrideEntry</span></span>

## <span data-ttu-id="06d64-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="06d64-111">PARAMETERS</span></span>

### <span data-ttu-id="06d64-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06d64-112">-DefaultProfile</span></span>
<span data-ttu-id="06d64-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="06d64-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06d64-114">-Regel</span><span class="sxs-lookup"><span data-stu-id="06d64-114">-Rule</span></span>
<span data-ttu-id="06d64-115">Liste der Regeln.</span><span class="sxs-lookup"><span data-stu-id="06d64-115">List of Rules.</span></span>

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

### <span data-ttu-id="06d64-116">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="06d64-116">-RuleGroupName</span></span>
<span data-ttu-id="06d64-117">Geben Sie die RegelGroupName in einem Eintrag zur Außerkraftsetzung der Regelgruppe an.</span><span class="sxs-lookup"><span data-stu-id="06d64-117">Specify the ruleGroupName in a override RuleGroup entry.</span></span>

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

### <span data-ttu-id="06d64-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06d64-118">CommonParameters</span></span>
<span data-ttu-id="06d64-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06d64-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06d64-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06d64-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06d64-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="06d64-121">INPUTS</span></span>

### <span data-ttu-id="06d64-122">Keine</span><span class="sxs-lookup"><span data-stu-id="06d64-122">None</span></span>

## <span data-ttu-id="06d64-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="06d64-123">OUTPUTS</span></span>

### <span data-ttu-id="06d64-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="06d64-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="06d64-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="06d64-125">NOTES</span></span>

## <span data-ttu-id="06d64-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="06d64-126">RELATED LINKS</span></span>
