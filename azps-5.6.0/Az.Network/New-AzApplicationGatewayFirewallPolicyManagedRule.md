---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRule.md
ms.openlocfilehash: 73404a44ea26a07aad2869cc8fc94ef1c74ee987
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935659"
---
# <span data-ttu-id="5885c-101">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="5885c-101">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>

## <span data-ttu-id="5885c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5885c-102">SYNOPSIS</span></span>
<span data-ttu-id="5885c-103">Erstellen Sie ManagedRules für die Firewallrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="5885c-103">Create ManagedRules for the firewall policy.</span></span>

## <span data-ttu-id="5885c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5885c-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRule
 [-ManagedRuleSet <PSApplicationGatewayFirewallPolicyManagedRuleSet[]>]
 [-Exclusion <PSApplicationGatewayFirewallPolicyExclusion[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5885c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5885c-105">DESCRIPTION</span></span>
<span data-ttu-id="5885c-106">Die **New-AzApplicationGatewayFirewallPolicyManagedRule** erstellt verwaltete Regeln für eine Firewallrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="5885c-106">The **New-AzApplicationGatewayFirewallPolicyManagedRule** creates a managed-rules for a firewall policy.</span></span>

## <span data-ttu-id="5885c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5885c-107">EXAMPLES</span></span>

### <span data-ttu-id="5885c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5885c-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallPolicyManagedRule -ManagedRuleSet $managedRuleSet -Exclusion $exclusion1,$exclusion2
```

<span data-ttu-id="5885c-109">Der Befehl erstellt verwaltete Regeln eine Liste von ManagedRuleSet mit $managedRuleSet und eine Ausschlussliste mit Einträgen als $exclusion 1, $exclusion 2.</span><span class="sxs-lookup"><span data-stu-id="5885c-109">The command creates managed rules a list of ManagedRuleSet with $managedRuleSet and an exclusion list with entries as $exclusion1, $exclusion2.</span></span>

## <span data-ttu-id="5885c-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5885c-110">PARAMETERS</span></span>

### <span data-ttu-id="5885c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5885c-111">-DefaultProfile</span></span>
<span data-ttu-id="5885c-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5885c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5885c-113">-Ausschluss</span><span class="sxs-lookup"><span data-stu-id="5885c-113">-Exclusion</span></span>
<span data-ttu-id="5885c-114">Liste des Ausschlusseintrags.</span><span class="sxs-lookup"><span data-stu-id="5885c-114">List of Exclusion Entry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyExclusion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5885c-115">-ManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="5885c-115">-ManagedRuleSet</span></span>
<span data-ttu-id="5885c-116">Liste der verwalteten RegelSets.</span><span class="sxs-lookup"><span data-stu-id="5885c-116">List of Managed ruleSets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleSet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5885c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5885c-117">CommonParameters</span></span>
<span data-ttu-id="5885c-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5885c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5885c-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5885c-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5885c-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5885c-120">INPUTS</span></span>

### <span data-ttu-id="5885c-121">Keine</span><span class="sxs-lookup"><span data-stu-id="5885c-121">None</span></span>

## <span data-ttu-id="5885c-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5885c-122">OUTPUTS</span></span>

### <span data-ttu-id="5885c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span><span class="sxs-lookup"><span data-stu-id="5885c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span></span>

## <span data-ttu-id="5885c-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5885c-124">NOTES</span></span>

## <span data-ttu-id="5885c-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5885c-125">RELATED LINKS</span></span>
