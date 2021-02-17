---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
ms.openlocfilehash: a3e057b8fbf6b04f48936b2aa96e9696964e5061
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146964"
---
# <span data-ttu-id="a52ab-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="a52ab-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="a52ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a52ab-102">SYNOPSIS</span></span>
<span data-ttu-id="a52ab-103">Erstellt einen managedRuleOverride-Eintrag für den Eintrag "RuleGroupOverrideGroup".</span><span class="sxs-lookup"><span data-stu-id="a52ab-103">Creates a managedRuleOverride entry for RuleGroupOverrideGroup entry.</span></span>

## <span data-ttu-id="a52ab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a52ab-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId <String> [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a52ab-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a52ab-105">DESCRIPTION</span></span>
<span data-ttu-id="a52ab-106">Die **Neue-AzApplicationGatewayFirewallPolicyManagedRuleOverride** erstellt einen "ruleOverride"-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="a52ab-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleOverride** creates a ruleOverride entry.</span></span>

## <span data-ttu-id="a52ab-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a52ab-107">EXAMPLES</span></span>

### <span data-ttu-id="a52ab-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a52ab-108">Example 1</span></span>
```powershell
PS C:\> ruleOverrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId $ruleId -State Disabled
```

<span data-ttu-id="a52ab-109">Erstellt einen ruleOverride-Eintrag mit "RuleId" $ruleId "State" als "Disabled".</span><span class="sxs-lookup"><span data-stu-id="a52ab-109">Creates a ruleOverride Entry with RuleId as $ruleId and State as Disabled.</span></span>

## <span data-ttu-id="a52ab-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a52ab-110">PARAMETERS</span></span>

### <span data-ttu-id="a52ab-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a52ab-111">-DefaultProfile</span></span>
<span data-ttu-id="a52ab-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a52ab-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a52ab-113">-RuleId</span><span class="sxs-lookup"><span data-stu-id="a52ab-113">-RuleId</span></span>
<span data-ttu-id="a52ab-114">Geben Sie die Regel-ID im Eintrag für die Außerkraftsetzungsregel an.</span><span class="sxs-lookup"><span data-stu-id="a52ab-114">Specify the RuleId in override rule entry.</span></span>

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

### <span data-ttu-id="a52ab-115">-State</span><span class="sxs-lookup"><span data-stu-id="a52ab-115">-State</span></span>
<span data-ttu-id="a52ab-116">Geben Sie die Regel-ID im Eintrag für die Außerkraftsetzungsregel an.</span><span class="sxs-lookup"><span data-stu-id="a52ab-116">Specify the RuleId in override rule entry.</span></span>

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

### <span data-ttu-id="a52ab-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a52ab-117">CommonParameters</span></span>
<span data-ttu-id="a52ab-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a52ab-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a52ab-119">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a52ab-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a52ab-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a52ab-120">INPUTS</span></span>

### <span data-ttu-id="a52ab-121">Keine</span><span class="sxs-lookup"><span data-stu-id="a52ab-121">None</span></span>

## <span data-ttu-id="a52ab-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a52ab-122">OUTPUTS</span></span>

### <span data-ttu-id="a52ab-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="a52ab-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="a52ab-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a52ab-124">NOTES</span></span>

## <span data-ttu-id="a52ab-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a52ab-125">RELATED LINKS</span></span>
