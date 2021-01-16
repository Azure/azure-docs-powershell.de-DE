---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleSet.md
ms.openlocfilehash: 3f4faec6b2af39f3386ec39e7df2e5bebcfe4277
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98302163"
---
# <span data-ttu-id="f664d-101">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="f664d-101">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>

## <span data-ttu-id="f664d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f664d-102">SYNOPSIS</span></span>
<span data-ttu-id="f664d-103">Erstellt ein ManagedRuleSet für die firewallPolicy</span><span class="sxs-lookup"><span data-stu-id="f664d-103">Creates a ManagedRuleSet for the firewallPolicy</span></span>

## <span data-ttu-id="f664d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f664d-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleSet -RuleSetType <String> -RuleSetVersion <String>
 [-RuleGroupOverride <PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f664d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f664d-105">DESCRIPTION</span></span>
<span data-ttu-id="f664d-106">Das **New-AzApplicationGatewayFirewallPolicyManagedRuleSet** erstellt verwaltete Regeln für eine Firewallrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="f664d-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleSet** creates a managed-rules for a firewall policy.</span></span>

## <span data-ttu-id="f664d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f664d-107">EXAMPLES</span></span>

### <span data-ttu-id="f664d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f664d-108">Example 1</span></span>
```powershell
PS C:\> $managedRuleSet = New-AzApplicationGatewayFirewallPolicyManagedRuleSet -RuleSetType $ruleSetType 
-RuleSetVersion $ruleSetVersion -RuleGroupOverrides $ruleGroupOverride1, $ruleGroupOverride2
```

<span data-ttu-id="f664d-109">Erstellt ein ManagedRuleSet mit "ruleSetType" als $ruleSetType, "ruleSetVersion" als $ruleSetVersion und "RuleGroupOverrides" als Liste mit Ganzen als $ruleGroupOverride 1, $ruleGroupOverride 2 Das neue "ManagedRuleSet" wird $managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="f664d-109">Creates a ManagedRuleSet with ruleSetType as $ruleSetType, ruleSetVersion as $ruleSetVersion and RuleGroupOverrides as a list with entires as $ruleGroupOverride1, $ruleGroupOverride2 The new ManagedRuleSet is assigned to $managedRuleSet</span></span>

## <span data-ttu-id="f664d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f664d-110">PARAMETERS</span></span>

### <span data-ttu-id="f664d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f664d-111">-DefaultProfile</span></span>
<span data-ttu-id="f664d-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f664d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f664d-113">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="f664d-113">-RuleGroupOverride</span></span>
<span data-ttu-id="f664d-114">Außerkraftsetzungen von Regelgruppen</span><span class="sxs-lookup"><span data-stu-id="f664d-114">Rule Group Overrides.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f664d-115">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="f664d-115">-RuleSetType</span></span>
<span data-ttu-id="f664d-116">Angeben des RuleSetType in einem managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="f664d-116">Specify the RuleSetType in a managedRuleSet</span></span>

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

### <span data-ttu-id="f664d-117">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="f664d-117">-RuleSetVersion</span></span>
<span data-ttu-id="f664d-118">Angeben von "RuleSetVersion" in einem managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="f664d-118">Specify the RuleSetVersion in a managedRuleSet</span></span>

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

### <span data-ttu-id="f664d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f664d-119">CommonParameters</span></span>
<span data-ttu-id="f664d-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f664d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f664d-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f664d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f664d-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f664d-122">INPUTS</span></span>

### <span data-ttu-id="f664d-123">Keine</span><span class="sxs-lookup"><span data-stu-id="f664d-123">None</span></span>

## <span data-ttu-id="f664d-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f664d-124">OUTPUTS</span></span>

### <span data-ttu-id="f664d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="f664d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleSet</span></span>

## <span data-ttu-id="f664d-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f664d-126">NOTES</span></span>

## <span data-ttu-id="f664d-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f664d-127">RELATED LINKS</span></span>
