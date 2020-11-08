---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrulegroupoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride.md
ms.openlocfilehash: 81b09a392464a004030a0798ea211db08a60a9f4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174600"
---
# <span data-ttu-id="7d099-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="7d099-101">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="7d099-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7d099-102">SYNOPSIS</span></span>
<span data-ttu-id="7d099-103">Erstellt RuleGroupOverride-Eintrag in ManagedRuleSets für die Firewall-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="7d099-103">Creates RuleGroupOverride entry in ManagedRuleSets for the firewall policy.</span></span>

## <span data-ttu-id="7d099-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d099-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName <String>
 -Rule <PSApplicationGatewayFirewallPolicyManagedRuleOverride[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7d099-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7d099-105">DESCRIPTION</span></span>
<span data-ttu-id="7d099-106">Der **New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** erstellt einen ruleGroupOverride-Eintrag in einem managedRuleSet für eine Firewall-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="7d099-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride** creates a ruleGroupOverride entry in a managedRuleSet for a firewall policy.</span></span>

## <span data-ttu-id="7d099-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7d099-107">EXAMPLES</span></span>

### <span data-ttu-id="7d099-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7d099-108">Example 1</span></span>
```powershell
PS C:\> $overrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride -RuleGroupName $ruleName -Rules $rule1,$rule2
```

<span data-ttu-id="7d099-109">Erstellt einen RuleGroupOverride-Eintrag mit Gruppennamen als $RuleName und Regeln als $Rule 1, $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="7d099-109">Creates a RuleGroupOverride entry with group name as $ruleName and Rules as $rule1, $rule2.</span></span> <span data-ttu-id="7d099-110">Weist $overrideEntry</span><span class="sxs-lookup"><span data-stu-id="7d099-110">Assigns the same to $overrideEntry</span></span>

## <span data-ttu-id="7d099-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d099-111">PARAMETERS</span></span>

### <span data-ttu-id="7d099-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d099-112">-DefaultProfile</span></span>
<span data-ttu-id="7d099-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7d099-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d099-114">-Rule</span><span class="sxs-lookup"><span data-stu-id="7d099-114">-Rule</span></span>
<span data-ttu-id="7d099-115">Liste der Regeln.</span><span class="sxs-lookup"><span data-stu-id="7d099-115">List of Rules.</span></span>

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

### <span data-ttu-id="7d099-116">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="7d099-116">-RuleGroupName</span></span>
<span data-ttu-id="7d099-117">Geben Sie die ruleGroupName in einem override rulegroup-Eintrag an.</span><span class="sxs-lookup"><span data-stu-id="7d099-117">Specify the ruleGroupName in a override RuleGroup entry.</span></span>

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

### <span data-ttu-id="7d099-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d099-118">CommonParameters</span></span>
<span data-ttu-id="7d099-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d099-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d099-120">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7d099-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d099-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7d099-121">INPUTS</span></span>

### <span data-ttu-id="7d099-122">Keine</span><span class="sxs-lookup"><span data-stu-id="7d099-122">None</span></span>

## <span data-ttu-id="7d099-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7d099-123">OUTPUTS</span></span>

### <span data-ttu-id="7d099-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="7d099-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>

## <span data-ttu-id="7d099-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="7d099-125">NOTES</span></span>

## <span data-ttu-id="7d099-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7d099-126">RELATED LINKS</span></span>
