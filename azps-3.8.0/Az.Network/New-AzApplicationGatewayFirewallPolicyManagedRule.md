---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicymanagedrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicyManagedRule.md
ms.openlocfilehash: 6b709283024a37d85bfac89f7e2fec4448544729
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94005022"
---
# <span data-ttu-id="a55c2-101">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="a55c2-101">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>

## <span data-ttu-id="a55c2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a55c2-102">SYNOPSIS</span></span>
<span data-ttu-id="a55c2-103">Erstellen Sie ManagedRules für die Firewall-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="a55c2-103">Create ManagedRules for the firewall policy.</span></span>

## <span data-ttu-id="a55c2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a55c2-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicyManagedRule
 [-ManagedRuleSet <PSApplicationGatewayFirewallPolicyManagedRuleSet[]>]
 [-Exclusion <PSApplicationGatewayFirewallPolicyExclusion[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a55c2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a55c2-105">DESCRIPTION</span></span>
<span data-ttu-id="a55c2-106">Das **neue AzApplicationGatewayFirewallPolicyManagedRule** erstellt eine Managed-Rules für eine Firewall-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="a55c2-106">The **New-AzApplicationGatewayFirewallPolicyManagedRule** creates a managed-rules for a firewall policy.</span></span>

## <span data-ttu-id="a55c2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a55c2-107">EXAMPLES</span></span>

### <span data-ttu-id="a55c2-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a55c2-108">Example 1</span></span>
```powershell
PS C:\> $condition = New-AzApplicationGatewayFirewallPolicyManagedRule -ManagedRuleSet $managedRuleSet -Exclusion $exclusion1,$exclusion2
```

<span data-ttu-id="a55c2-109">Mit dem Befehl werden verwaltete Regeln erstellt, eine Liste von ManagedRuleSet mit $managedRuleSet und eine Ausschlussliste mit Einträgen als $Exclusion 1, $Exclusion 2.</span><span class="sxs-lookup"><span data-stu-id="a55c2-109">The command creates managed rules a list of ManagedRuleSet with $managedRuleSet and an exclusion list with entries as $exclusion1, $exclusion2.</span></span>

## <span data-ttu-id="a55c2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a55c2-110">PARAMETERS</span></span>

### <span data-ttu-id="a55c2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a55c2-111">-DefaultProfile</span></span>
<span data-ttu-id="a55c2-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a55c2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a55c2-113">– Ausschluss</span><span class="sxs-lookup"><span data-stu-id="a55c2-113">-Exclusion</span></span>
<span data-ttu-id="a55c2-114">Liste des Ausschluss Eintrags.</span><span class="sxs-lookup"><span data-stu-id="a55c2-114">List of Exclusion Entry.</span></span>

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

### <span data-ttu-id="a55c2-115">-ManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="a55c2-115">-ManagedRuleSet</span></span>
<span data-ttu-id="a55c2-116">Liste verwalteter RuleSets.</span><span class="sxs-lookup"><span data-stu-id="a55c2-116">List of Managed ruleSets.</span></span>

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

### <span data-ttu-id="a55c2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a55c2-117">CommonParameters</span></span>
<span data-ttu-id="a55c2-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a55c2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a55c2-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a55c2-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a55c2-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a55c2-120">INPUTS</span></span>

### <span data-ttu-id="a55c2-121">Keine</span><span class="sxs-lookup"><span data-stu-id="a55c2-121">None</span></span>

## <span data-ttu-id="a55c2-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a55c2-122">OUTPUTS</span></span>

### <span data-ttu-id="a55c2-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallPolicyManagedRules</span><span class="sxs-lookup"><span data-stu-id="a55c2-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span></span>

## <span data-ttu-id="a55c2-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="a55c2-124">NOTES</span></span>

## <span data-ttu-id="a55c2-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a55c2-125">RELATED LINKS</span></span>
