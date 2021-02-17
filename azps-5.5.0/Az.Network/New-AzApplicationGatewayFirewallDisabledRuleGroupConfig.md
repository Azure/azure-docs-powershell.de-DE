---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewalldisabledrulegroupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
ms.openlocfilehash: 5eafcfc825b710e31954e247e4114d0f90e97c41
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147017"
---
# <span data-ttu-id="a059b-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span><span class="sxs-lookup"><span data-stu-id="a059b-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>

## <span data-ttu-id="a059b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a059b-102">SYNOPSIS</span></span>
<span data-ttu-id="a059b-103">Erstellt eine neue deaktivierte Regelgruppenkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="a059b-103">Creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="a059b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a059b-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName <String> [-Rules <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a059b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a059b-105">DESCRIPTION</span></span>
<span data-ttu-id="a059b-106">Das **Cmdlet "New-AzApplicationGatewayFirewallDisabledRuleGroupConfig"** erstellt eine neue deaktivierte Regelgruppenkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="a059b-106">The **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="a059b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a059b-107">EXAMPLES</span></span>

### <span data-ttu-id="a059b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a059b-108">Example 1</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
```

<span data-ttu-id="a059b-109">Der Befehl erstellt eine neue deaktivierte Regelgruppenkonfiguration für die Regelgruppe "REQUEST-942-APPLICATION-ATTACK-SQLI", in der Regel 942130 und Regel 942140 deaktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="a059b-109">The command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span> <span data-ttu-id="a059b-110">Die Konfiguration der neuen deaktivierten Regelgruppe wird in $disabledRuleGroup gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a059b-110">The new disabled rule group configuration is saved in $disabledRuleGroup1.</span></span>

## <span data-ttu-id="a059b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a059b-111">PARAMETERS</span></span>

### <span data-ttu-id="a059b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a059b-112">-DefaultProfile</span></span>
<span data-ttu-id="a059b-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a059b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a059b-114">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="a059b-114">-RuleGroupName</span></span>
<span data-ttu-id="a059b-115">Der Name der Regelgruppe, die deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="a059b-115">The name of the rule group that will be disabled.</span></span>

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

### <span data-ttu-id="a059b-116">-Regeln</span><span class="sxs-lookup"><span data-stu-id="a059b-116">-Rules</span></span>
<span data-ttu-id="a059b-117">Die Liste der Regeln, die deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="a059b-117">The list of rules that will be disabled.</span></span>
<span data-ttu-id="a059b-118">Wenn null, werden alle Regeln der Regelgruppe deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a059b-118">If null, all rules of the rule group will be disabled.</span></span>

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

### <span data-ttu-id="a059b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a059b-119">CommonParameters</span></span>
<span data-ttu-id="a059b-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a059b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a059b-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a059b-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a059b-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a059b-122">INPUTS</span></span>

### <span data-ttu-id="a059b-123">Keine</span><span class="sxs-lookup"><span data-stu-id="a059b-123">None</span></span>

## <span data-ttu-id="a059b-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a059b-124">OUTPUTS</span></span>

### <span data-ttu-id="a059b-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="a059b-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span></span>

## <span data-ttu-id="a059b-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a059b-126">NOTES</span></span>

## <span data-ttu-id="a059b-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a059b-127">RELATED LINKS</span></span>

[<span data-ttu-id="a059b-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="a059b-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="a059b-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="a059b-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

