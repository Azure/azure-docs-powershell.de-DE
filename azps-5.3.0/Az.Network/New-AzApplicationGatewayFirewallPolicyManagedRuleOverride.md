---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
ms.openlocfilehash: a3e057b8fbf6b04f48936b2aa96e9696964e5061
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385620"
---
# <span data-ttu-id="f765e-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="f765e-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="f765e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f765e-102">SYNOPSIS</span></span>
<span data-ttu-id="f765e-103">Erstellt einen managedRuleOverride-Eintrag für den Eintrag "RuleGroupOverrideGroup".</span><span class="sxs-lookup"><span data-stu-id="f765e-103">Creates a managedRuleOverride entry for RuleGroupOverrideGroup entry.</span></span>

## <span data-ttu-id="f765e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f765e-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId <String> [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f765e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f765e-105">DESCRIPTION</span></span>
<span data-ttu-id="f765e-106">Die **Neue-AzApplicationGatewayFirewallPolicyManagedRuleOverride** erstellt einen "ruleOverride"-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="f765e-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleOverride** creates a ruleOverride entry.</span></span>

## <span data-ttu-id="f765e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f765e-107">EXAMPLES</span></span>

### <span data-ttu-id="f765e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f765e-108">Example 1</span></span>
```powershell
PS C:\> ruleOverrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId $ruleId -State Disabled
```

<span data-ttu-id="f765e-109">Erstellt einen ruleOverride-Eintrag mit "RuleId" als $ruleId "State" als "Disabled".</span><span class="sxs-lookup"><span data-stu-id="f765e-109">Creates a ruleOverride Entry with RuleId as $ruleId and State as Disabled.</span></span>

## <span data-ttu-id="f765e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f765e-110">PARAMETERS</span></span>

### <span data-ttu-id="f765e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f765e-111">-DefaultProfile</span></span>
<span data-ttu-id="f765e-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f765e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f765e-113">-RuleId</span><span class="sxs-lookup"><span data-stu-id="f765e-113">-RuleId</span></span>
<span data-ttu-id="f765e-114">Geben Sie die Regel-ID im Eintrag "Regel außer Kraft" an.</span><span class="sxs-lookup"><span data-stu-id="f765e-114">Specify the RuleId in override rule entry.</span></span>

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

### <span data-ttu-id="f765e-115">-State</span><span class="sxs-lookup"><span data-stu-id="f765e-115">-State</span></span>
<span data-ttu-id="f765e-116">Geben Sie die Regel-ID im Eintrag "Regel außer Kraft" an.</span><span class="sxs-lookup"><span data-stu-id="f765e-116">Specify the RuleId in override rule entry.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Disabled

Required: False
Position: Named
Default value: Disabled
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f765e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f765e-117">CommonParameters</span></span>
<span data-ttu-id="f765e-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f765e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f765e-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f765e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f765e-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f765e-120">INPUTS</span></span>

### <span data-ttu-id="f765e-121">Keine</span><span class="sxs-lookup"><span data-stu-id="f765e-121">None</span></span>

## <span data-ttu-id="f765e-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f765e-122">OUTPUTS</span></span>

### <span data-ttu-id="f765e-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="f765e-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="f765e-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f765e-124">NOTES</span></span>

## <span data-ttu-id="f765e-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f765e-125">RELATED LINKS</span></span>
