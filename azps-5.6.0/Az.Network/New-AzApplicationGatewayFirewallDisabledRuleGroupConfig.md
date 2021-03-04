---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfirewalldisabledrulegroupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
ms.openlocfilehash: 5a96ea5ac1ded346e289d44f54762909d5f96e31
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918712"
---
# <span data-ttu-id="10782-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span><span class="sxs-lookup"><span data-stu-id="10782-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>

## <span data-ttu-id="10782-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10782-102">SYNOPSIS</span></span>
<span data-ttu-id="10782-103">Erstellt eine neue deaktivierte Regelgruppenkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="10782-103">Creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="10782-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="10782-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName <String> [-Rules <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10782-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10782-105">DESCRIPTION</span></span>
<span data-ttu-id="10782-106">Das **Cmdlet New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** erstellt eine neue deaktivierte Regelgruppenkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="10782-106">The **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="10782-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="10782-107">EXAMPLES</span></span>

### <span data-ttu-id="10782-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="10782-108">Example 1</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
```

<span data-ttu-id="10782-109">Der Befehl erstellt eine neue deaktivierte Regelgruppenkonfiguration für die Regelgruppe mit dem Namen "REQUEST-942-APPLICATION-ATTACK-SQLI", bei der Regel 942130 und Regel 942140 deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="10782-109">The command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span> <span data-ttu-id="10782-110">Die konfiguration der neuen deaktivierten Regelgruppe wird in $disabledRuleGroup 1 gespeichert.</span><span class="sxs-lookup"><span data-stu-id="10782-110">The new disabled rule group configuration is saved in $disabledRuleGroup1.</span></span>

## <span data-ttu-id="10782-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="10782-111">PARAMETERS</span></span>

### <span data-ttu-id="10782-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10782-112">-DefaultProfile</span></span>
<span data-ttu-id="10782-113">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="10782-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10782-114">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="10782-114">-RuleGroupName</span></span>
<span data-ttu-id="10782-115">Der Name der Regelgruppe, die deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="10782-115">The name of the rule group that will be disabled.</span></span>

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

### <span data-ttu-id="10782-116">-Regeln</span><span class="sxs-lookup"><span data-stu-id="10782-116">-Rules</span></span>
<span data-ttu-id="10782-117">Die Liste der Regeln, die deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="10782-117">The list of rules that will be disabled.</span></span>
<span data-ttu-id="10782-118">Ist Null, werden alle Regeln der Regelgruppe deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="10782-118">If null, all rules of the rule group will be disabled.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10782-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10782-119">CommonParameters</span></span>
<span data-ttu-id="10782-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10782-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10782-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10782-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10782-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="10782-122">INPUTS</span></span>

### <span data-ttu-id="10782-123">Keine</span><span class="sxs-lookup"><span data-stu-id="10782-123">None</span></span>

## <span data-ttu-id="10782-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="10782-124">OUTPUTS</span></span>

### <span data-ttu-id="10782-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="10782-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span></span>

## <span data-ttu-id="10782-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="10782-126">NOTES</span></span>

## <span data-ttu-id="10782-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="10782-127">RELATED LINKS</span></span>

[<span data-ttu-id="10782-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="10782-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="10782-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="10782-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

