---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleoverride
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleOverride.md
ms.openlocfilehash: a3e057b8fbf6b04f48936b2aa96e9696964e5061
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009686"
---
# <span data-ttu-id="4bd65-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="4bd65-101">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="4bd65-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4bd65-102">SYNOPSIS</span></span>
<span data-ttu-id="4bd65-103">Erstellt einen managedRuleOverride-Eintrag für den RuleGroupOverrideGroup-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="4bd65-103">Creates a managedRuleOverride entry for RuleGroupOverrideGroup entry.</span></span>

## <span data-ttu-id="4bd65-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4bd65-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId <String> [-State <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bd65-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4bd65-105">DESCRIPTION</span></span>
<span data-ttu-id="4bd65-106">Der **New-AzApplicationGatewayFirewallPolicyManagedRuleOverride** erstellt einen ruleOverride-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="4bd65-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleOverride** creates a ruleOverride entry.</span></span>

## <span data-ttu-id="4bd65-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4bd65-107">EXAMPLES</span></span>

### <span data-ttu-id="4bd65-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4bd65-108">Example 1</span></span>
```powershell
PS C:\> ruleOverrideEntry = New-AzApplicationGatewayFirewallPolicyManagedRuleOverride -RuleId $ruleId -State Disabled
```

<span data-ttu-id="4bd65-109">Erstellt einen ruleOverride-Eintrag mit der Option "Lineal" als $ruleId und Zustand als deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="4bd65-109">Creates a ruleOverride Entry with RuleId as $ruleId and State as Disabled.</span></span>

## <span data-ttu-id="4bd65-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4bd65-110">PARAMETERS</span></span>

### <span data-ttu-id="4bd65-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bd65-111">-DefaultProfile</span></span>
<span data-ttu-id="4bd65-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4bd65-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bd65-113">-Lineal</span><span class="sxs-lookup"><span data-stu-id="4bd65-113">-RuleId</span></span>
<span data-ttu-id="4bd65-114">Geben Sie den Eintrag Rule-Nr in override Rule an.</span><span class="sxs-lookup"><span data-stu-id="4bd65-114">Specify the RuleId in override rule entry.</span></span>

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

### <span data-ttu-id="4bd65-115">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="4bd65-115">-State</span></span>
<span data-ttu-id="4bd65-116">Geben Sie den Eintrag Rule-Nr in override Rule an.</span><span class="sxs-lookup"><span data-stu-id="4bd65-116">Specify the RuleId in override rule entry.</span></span>

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

### <span data-ttu-id="4bd65-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bd65-117">CommonParameters</span></span>
<span data-ttu-id="4bd65-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bd65-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bd65-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4bd65-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bd65-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4bd65-120">INPUTS</span></span>

### <span data-ttu-id="4bd65-121">Keine</span><span class="sxs-lookup"><span data-stu-id="4bd65-121">None</span></span>

## <span data-ttu-id="4bd65-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4bd65-122">OUTPUTS</span></span>

### <span data-ttu-id="4bd65-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="4bd65-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>

## <span data-ttu-id="4bd65-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="4bd65-124">NOTES</span></span>

## <span data-ttu-id="4bd65-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4bd65-125">RELATED LINKS</span></span>
