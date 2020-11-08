---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewalldisabledrulegroupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
ms.openlocfilehash: 5eafcfc825b710e31954e247e4114d0f90e97c41
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94005039"
---
# <span data-ttu-id="c37c8-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span><span class="sxs-lookup"><span data-stu-id="c37c8-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>

## <span data-ttu-id="c37c8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c37c8-102">SYNOPSIS</span></span>
<span data-ttu-id="c37c8-103">Erstellt eine neue deaktivierte Regelgruppen Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="c37c8-103">Creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="c37c8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c37c8-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName <String> [-Rules <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c37c8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c37c8-105">DESCRIPTION</span></span>
<span data-ttu-id="c37c8-106">Das Cmdlet **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** erstellt eine neue deaktivierte Regelgruppen Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="c37c8-106">The **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="c37c8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c37c8-107">EXAMPLES</span></span>

### <span data-ttu-id="c37c8-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c37c8-108">Example 1</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
```

<span data-ttu-id="c37c8-109">Der Befehl erstellt eine neue deaktivierte Regelgruppen Konfiguration für die Regelgruppe mit dem Namen "Request-942-Application-Attack-SQLI" mit der Regel 942130 und der Regel 942140, die deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="c37c8-109">The command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span> <span data-ttu-id="c37c8-110">Die Konfiguration der neuen deaktivierten Regelgruppe wird in $disabledRuleGroup 1 gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c37c8-110">The new disabled rule group configuration is saved in $disabledRuleGroup1.</span></span>

## <span data-ttu-id="c37c8-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="c37c8-111">PARAMETERS</span></span>

### <span data-ttu-id="c37c8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c37c8-112">-DefaultProfile</span></span>
<span data-ttu-id="c37c8-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c37c8-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c37c8-114">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="c37c8-114">-RuleGroupName</span></span>
<span data-ttu-id="c37c8-115">Der Name der Regelgruppe, die deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c37c8-115">The name of the rule group that will be disabled.</span></span>

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

### <span data-ttu-id="c37c8-116">-Regeln</span><span class="sxs-lookup"><span data-stu-id="c37c8-116">-Rules</span></span>
<span data-ttu-id="c37c8-117">Die Liste der Regeln, die deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="c37c8-117">The list of rules that will be disabled.</span></span>
<span data-ttu-id="c37c8-118">Ist NULL, werden alle Regeln der Regelgruppe deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c37c8-118">If null, all rules of the rule group will be disabled.</span></span>

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

### <span data-ttu-id="c37c8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c37c8-119">CommonParameters</span></span>
<span data-ttu-id="c37c8-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c37c8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c37c8-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c37c8-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c37c8-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c37c8-122">INPUTS</span></span>

### <span data-ttu-id="c37c8-123">Keine</span><span class="sxs-lookup"><span data-stu-id="c37c8-123">None</span></span>

## <span data-ttu-id="c37c8-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c37c8-124">OUTPUTS</span></span>

### <span data-ttu-id="c37c8-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallDisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="c37c8-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span></span>

## <span data-ttu-id="c37c8-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="c37c8-126">NOTES</span></span>

## <span data-ttu-id="c37c8-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c37c8-127">RELATED LINKS</span></span>

[<span data-ttu-id="c37c8-128">Neu – AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="c37c8-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="c37c8-129">Satz-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="c37c8-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

