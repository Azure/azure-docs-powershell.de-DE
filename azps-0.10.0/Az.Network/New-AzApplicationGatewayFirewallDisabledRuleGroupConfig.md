---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewalldisabledrulegroupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayFirewallDisabledRuleGroupConfig.md
ms.openlocfilehash: 5377eabbf027adf18c88204bef6be59c7cf411be
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841436"
---
# <span data-ttu-id="45df7-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span><span class="sxs-lookup"><span data-stu-id="45df7-101">New-AzApplicationGatewayFirewallDisabledRuleGroupConfig</span></span>

## <span data-ttu-id="45df7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="45df7-102">SYNOPSIS</span></span>
<span data-ttu-id="45df7-103">Erstellt eine neue deaktivierte Regelgruppen Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="45df7-103">Creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="45df7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="45df7-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName <String>
 [-Rules <System.Collections.Generic.List`1[System.Int32]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="45df7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="45df7-105">DESCRIPTION</span></span>
<span data-ttu-id="45df7-106">Das Cmdlet **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** erstellt eine neue deaktivierte Regelgruppen Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="45df7-106">The **New-AzApplicationGatewayFirewallDisabledRuleGroupConfig** cmdlet creates a new disabled rule group configuration.</span></span>

## <span data-ttu-id="45df7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="45df7-107">EXAMPLES</span></span>

### <span data-ttu-id="45df7-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="45df7-108">Example 1</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
```

<span data-ttu-id="45df7-109">Der Befehl erstellt eine neue deaktivierte Regelgruppen Konfiguration für die Regelgruppe mit dem Namen "Request-942-Application-Attack-SQLI" mit der Regel 942130 und der Regel 942140, die deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="45df7-109">The command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span> <span data-ttu-id="45df7-110">Die Konfiguration der neuen deaktivierten Regelgruppe wird in $disabledRuleGroup 1 gespeichert.</span><span class="sxs-lookup"><span data-stu-id="45df7-110">The new disabled rule group configuration is saved in $disabledRuleGroup1.</span></span>

## <span data-ttu-id="45df7-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="45df7-111">PARAMETERS</span></span>

### <span data-ttu-id="45df7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45df7-112">-DefaultProfile</span></span>
<span data-ttu-id="45df7-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="45df7-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45df7-114">-RuleGroupName</span><span class="sxs-lookup"><span data-stu-id="45df7-114">-RuleGroupName</span></span>
<span data-ttu-id="45df7-115">Der Name der Regelgruppe, die deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="45df7-115">The name of the rule group that will be disabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45df7-116">-Regeln</span><span class="sxs-lookup"><span data-stu-id="45df7-116">-Rules</span></span>
<span data-ttu-id="45df7-117">Die Liste der Regeln, die deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="45df7-117">The list of rules that will be disabled.</span></span>
<span data-ttu-id="45df7-118">Ist NULL, werden alle Regeln der Regelgruppe deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="45df7-118">If null, all rules of the rule group will be disabled.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45df7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45df7-119">CommonParameters</span></span>
<span data-ttu-id="45df7-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45df7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45df7-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45df7-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45df7-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="45df7-122">INPUTS</span></span>

### <span data-ttu-id="45df7-123">Keine</span><span class="sxs-lookup"><span data-stu-id="45df7-123">None</span></span>

## <span data-ttu-id="45df7-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="45df7-124">OUTPUTS</span></span>

### <span data-ttu-id="45df7-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallDisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="45df7-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup</span></span>

## <span data-ttu-id="45df7-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="45df7-126">NOTES</span></span>

## <span data-ttu-id="45df7-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="45df7-127">RELATED LINKS</span></span>

[<span data-ttu-id="45df7-128">Neu – AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="45df7-128">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="45df7-129">Satz-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="45df7-129">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

