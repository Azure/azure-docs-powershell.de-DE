---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 76DB6AF5-BF6F-436C-8500-626468F84466
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: bdfd9cb100b43f58326b9b94c4e15bb24561eadd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841375"
---
# <span data-ttu-id="35ab7-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="35ab7-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="35ab7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="35ab7-102">SYNOPSIS</span></span>
<span data-ttu-id="35ab7-103">Erstellt eine WAF-Konfiguration für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="35ab7-103">Creates a WAF configuration for an application gateway.</span></span>

## <span data-ttu-id="35ab7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="35ab7-104">SYNTAX</span></span>

```
New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled <Boolean> -FirewallMode <String>
 [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroups <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35ab7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="35ab7-105">DESCRIPTION</span></span>
<span data-ttu-id="35ab7-106">Das Cmdlet **New-AzApplicationGatewayWebApplicationFirewallConfiguration** erstellt eine WAF-Konfiguration (Web Application Firewall) für ein Azure Application-Gateway.</span><span class="sxs-lookup"><span data-stu-id="35ab7-106">The **New-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet creates a web application firewall (WAF) configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="35ab7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="35ab7-107">EXAMPLES</span></span>

### <span data-ttu-id="35ab7-108">Beispiel 1: Erstellen einer Webanwendungs Firewall-Konfiguration für ein Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="35ab7-108">Example 1: Create a web application firewall configuration for an application gateway</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
PS C:\> $disabledRuleGroup2 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-921-PROTOCOL-ATTACK"
PS C:\> $firewallConfig = New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled $true -FirewallMode "Prevention" -RuleSetType "OWASP" -RuleSetVersion "3.0" -DisabledRuleGroups $disabledRuleGroup1,$disabledRuleGroup2
```

<span data-ttu-id="35ab7-109">Mit dem ersten Befehl wird eine neue deaktivierte Regelgruppen Konfiguration für die Regelgruppe mit dem Namen "Request-942-Application-Attack-SQLI" erstellt, wobei Regel 942130 und Regel 942140 deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="35ab7-109">The first command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span>
<span data-ttu-id="35ab7-110">Mit dem zweiten Befehl wird eine weitere deaktivierte Regelgruppen Konfiguration für eine Regelgruppe mit dem Namen "Request-921-Protocol-Attack" erstellt.</span><span class="sxs-lookup"><span data-stu-id="35ab7-110">The second command creates another disabled rule group configuration for a rule group named "REQUEST-921-PROTOCOL-ATTACK".</span></span> <span data-ttu-id="35ab7-111">Es werden keine Regeln ausdrücklich übergeben, sodass alle Regeln der Regelgruppe deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="35ab7-111">No rules are specifically passed and thus all rules of the rule group will be disabled.</span></span>
<span data-ttu-id="35ab7-112">Der letzte Befehl erstellt dann eine WAF-Konfiguration mit deaktivierten Firewallregeln, die in $disabledRuleGroup 1 und $disabledRuleGroup 2 konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="35ab7-112">The last command then creates a WAF configuration with firewall rules disabled as configured in $disabledRuleGroup1 and $disabledRuleGroup2.</span></span> <span data-ttu-id="35ab7-113">Die neue WAF-Konfiguration wird in der $firewallConfig-Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="35ab7-113">The new WAF configuration is stored in the $firewallConfig variable.</span></span>

## <span data-ttu-id="35ab7-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="35ab7-114">PARAMETERS</span></span>

### <span data-ttu-id="35ab7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35ab7-115">-DefaultProfile</span></span>
<span data-ttu-id="35ab7-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="35ab7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35ab7-117">-DisabledRuleGroups</span><span class="sxs-lookup"><span data-stu-id="35ab7-117">-DisabledRuleGroups</span></span>
<span data-ttu-id="35ab7-118">Die deaktivierten Regelgruppen.</span><span class="sxs-lookup"><span data-stu-id="35ab7-118">The disabled rule groups.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35ab7-119">-Aktiviert</span><span class="sxs-lookup"><span data-stu-id="35ab7-119">-Enabled</span></span>
<span data-ttu-id="35ab7-120">Gibt an, ob die WAF aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="35ab7-120">Indicates whether the WAF is enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35ab7-121">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="35ab7-121">-FirewallMode</span></span>
<span data-ttu-id="35ab7-122">Gibt den Web Application Firewall-Modus an.</span><span class="sxs-lookup"><span data-stu-id="35ab7-122">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="35ab7-123">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="35ab7-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="35ab7-124">Erkennung</span><span class="sxs-lookup"><span data-stu-id="35ab7-124">Detection</span></span>
- <span data-ttu-id="35ab7-125">Prävention</span><span class="sxs-lookup"><span data-stu-id="35ab7-125">Prevention</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Detection, Prevention

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35ab7-126">-Rulesettype</span><span class="sxs-lookup"><span data-stu-id="35ab7-126">-RuleSetType</span></span>
<span data-ttu-id="35ab7-127">Der Typ des Webanwendungs-Firewallregel-Regelsatzes.</span><span class="sxs-lookup"><span data-stu-id="35ab7-127">The type of the web application firewall rule set.</span></span> <span data-ttu-id="35ab7-128">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="35ab7-128">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="35ab7-129">OWASP</span><span class="sxs-lookup"><span data-stu-id="35ab7-129">OWASP</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: OWASP

Required: False
Position: Named
Default value: OWASP
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35ab7-130">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="35ab7-130">-RuleSetVersion</span></span>
<span data-ttu-id="35ab7-131">Die Version des Regelsatztyps.</span><span class="sxs-lookup"><span data-stu-id="35ab7-131">The version of the rule set type.</span></span>
<span data-ttu-id="35ab7-132">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="35ab7-132">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="35ab7-133">3,0</span><span class="sxs-lookup"><span data-stu-id="35ab7-133">3.0</span></span>
- <span data-ttu-id="35ab7-134">2.2.9</span><span class="sxs-lookup"><span data-stu-id="35ab7-134">2.2.9</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 3.0, 2.2.9

Required: False
Position: Named
Default value: 3.0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35ab7-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="35ab7-135">-Confirm</span></span>
<span data-ttu-id="35ab7-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="35ab7-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35ab7-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35ab7-137">-WhatIf</span></span>
<span data-ttu-id="35ab7-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="35ab7-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="35ab7-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="35ab7-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35ab7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35ab7-140">CommonParameters</span></span>
<span data-ttu-id="35ab7-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35ab7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35ab7-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35ab7-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35ab7-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="35ab7-143">INPUTS</span></span>

## <span data-ttu-id="35ab7-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="35ab7-144">OUTPUTS</span></span>

### <span data-ttu-id="35ab7-145">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="35ab7-145">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="35ab7-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="35ab7-146">NOTES</span></span>

## <span data-ttu-id="35ab7-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="35ab7-147">RELATED LINKS</span></span>

[<span data-ttu-id="35ab7-148">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="35ab7-148">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="35ab7-149">Satz-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="35ab7-149">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


