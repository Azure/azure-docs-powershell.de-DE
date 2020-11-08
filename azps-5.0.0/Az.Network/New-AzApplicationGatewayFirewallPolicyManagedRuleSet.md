---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRuleSet.md
ms.openlocfilehash: 3f4faec6b2af39f3386ec39e7df2e5bebcfe4277
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179889"
---
# <span data-ttu-id="a9933-101">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="a9933-101">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>

## <span data-ttu-id="a9933-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a9933-102">SYNOPSIS</span></span>
<span data-ttu-id="a9933-103">Erstellt eine ManagedRuleSet für die firewallPolicy</span><span class="sxs-lookup"><span data-stu-id="a9933-103">Creates a ManagedRuleSet for the firewallPolicy</span></span>

## <span data-ttu-id="a9933-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9933-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRuleSet -RuleSetType <String> -RuleSetVersion <String>
 [-RuleGroupOverride <PSApplicationGatewayFirewallPolicyManagedRuleGroupOverride[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9933-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9933-105">DESCRIPTION</span></span>
<span data-ttu-id="a9933-106">Das **neue AzApplicationGatewayFirewallPolicyManagedRuleSet** erstellt eine Managed-Rules für eine Firewall-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="a9933-106">The **New-AzApplicationGatewayFirewallPolicyManagedRuleSet** creates a managed-rules for a firewall policy.</span></span>

## <span data-ttu-id="a9933-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a9933-107">EXAMPLES</span></span>

### <span data-ttu-id="a9933-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a9933-108">Example 1</span></span>
```powershell
PS C:\> $managedRuleSet = New-AzApplicationGatewayFirewallPolicyManagedRuleSet -RuleSetType $ruleSetType 
-RuleSetVersion $ruleSetVersion -RuleGroupOverrides $ruleGroupOverride1, $ruleGroupOverride2
```

<span data-ttu-id="a9933-109">Erstellt eine ManagedRuleSet mit rulesettype als $ruleSetType, ruleSetVersion als $ruleSetVersion und RuleGroupOverrides als eine Liste mit ganzen als $ruleGroupOverride 1, $ruleGroupOverride 2 der neuen ManagedRuleSet zugeordnet ist $managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="a9933-109">Creates a ManagedRuleSet with ruleSetType as $ruleSetType, ruleSetVersion as $ruleSetVersion and RuleGroupOverrides as a list with entires as $ruleGroupOverride1, $ruleGroupOverride2 The new ManagedRuleSet is assigned to $managedRuleSet</span></span>

## <span data-ttu-id="a9933-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9933-110">PARAMETERS</span></span>

### <span data-ttu-id="a9933-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9933-111">-DefaultProfile</span></span>
<span data-ttu-id="a9933-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a9933-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9933-113">-RuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="a9933-113">-RuleGroupOverride</span></span>
<span data-ttu-id="a9933-114">Regelgruppe Außerkraftsetzungen.</span><span class="sxs-lookup"><span data-stu-id="a9933-114">Rule Group Overrides.</span></span>

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

### <span data-ttu-id="a9933-115">-Rulesettype</span><span class="sxs-lookup"><span data-stu-id="a9933-115">-RuleSetType</span></span>
<span data-ttu-id="a9933-116">Angeben des rulesettype in einer managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="a9933-116">Specify the RuleSetType in a managedRuleSet</span></span>

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

### <span data-ttu-id="a9933-117">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="a9933-117">-RuleSetVersion</span></span>
<span data-ttu-id="a9933-118">Angeben des RuleSetVersion in einer managedRuleSet</span><span class="sxs-lookup"><span data-stu-id="a9933-118">Specify the RuleSetVersion in a managedRuleSet</span></span>

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

### <span data-ttu-id="a9933-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9933-119">CommonParameters</span></span>
<span data-ttu-id="a9933-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9933-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9933-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9933-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9933-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a9933-122">INPUTS</span></span>

### <span data-ttu-id="a9933-123">Keine</span><span class="sxs-lookup"><span data-stu-id="a9933-123">None</span></span>

## <span data-ttu-id="a9933-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a9933-124">OUTPUTS</span></span>

### <span data-ttu-id="a9933-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="a9933-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRuleSet</span></span>

## <span data-ttu-id="a9933-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="a9933-126">NOTES</span></span>

## <span data-ttu-id="a9933-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a9933-127">RELATED LINKS</span></span>
