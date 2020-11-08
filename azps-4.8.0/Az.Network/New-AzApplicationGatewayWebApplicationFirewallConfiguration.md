---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 76DB6AF5-BF6F-436C-8500-626468F84466
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 0f186de1ad548be0c566c6fac2b8d1505885bfe0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175071"
---
# <span data-ttu-id="72e50-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="72e50-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="72e50-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="72e50-102">SYNOPSIS</span></span>
<span data-ttu-id="72e50-103">Erstellt eine WAF-Konfiguration für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="72e50-103">Creates a WAF configuration for an application gateway.</span></span>

## <span data-ttu-id="72e50-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="72e50-104">SYNTAX</span></span>

```
New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled <Boolean> -FirewallMode <String>
 [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <PSApplicationGatewayFirewallDisabledRuleGroup[]>] [-RequestBodyCheck <Boolean>]
 [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <PSApplicationGatewayFirewallExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72e50-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="72e50-105">DESCRIPTION</span></span>
<span data-ttu-id="72e50-106">Das Cmdlet **New-AzApplicationGatewayWebApplicationFirewallConfiguration** erstellt eine WAF-Konfiguration (Web Application Firewall) für ein Azure Application-Gateway.</span><span class="sxs-lookup"><span data-stu-id="72e50-106">The **New-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet creates a web application firewall (WAF) configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="72e50-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="72e50-107">EXAMPLES</span></span>

### <span data-ttu-id="72e50-108">Beispiel 1: Erstellen einer Webanwendungs Firewall-Konfiguration für ein Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="72e50-108">Example 1: Create a web application firewall configuration for an application gateway</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
PS C:\> $disabledRuleGroup2 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-921-PROTOCOL-ATTACK"
PS C:\> $firewallConfig = New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled $true -FirewallMode "Prevention" -RuleSetType "OWASP" -RuleSetVersion "3.0" -DisabledRuleGroups $disabledRuleGroup1,$disabledRuleGroup2
```

<span data-ttu-id="72e50-109">Mit dem ersten Befehl wird eine neue deaktivierte Regelgruppen Konfiguration für die Regelgruppe mit dem Namen "Request-942-Application-Attack-SQLI" erstellt, wobei Regel 942130 und Regel 942140 deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="72e50-109">The first command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span>
<span data-ttu-id="72e50-110">Mit dem zweiten Befehl wird eine weitere deaktivierte Regelgruppen Konfiguration für eine Regelgruppe mit dem Namen "Request-921-Protocol-Attack" erstellt.</span><span class="sxs-lookup"><span data-stu-id="72e50-110">The second command creates another disabled rule group configuration for a rule group named "REQUEST-921-PROTOCOL-ATTACK".</span></span> <span data-ttu-id="72e50-111">Es werden keine Regeln ausdrücklich übergeben, sodass alle Regeln der Regelgruppe deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="72e50-111">No rules are specifically passed and thus all rules of the rule group will be disabled.</span></span>
<span data-ttu-id="72e50-112">Der letzte Befehl erstellt dann eine WAF-Konfiguration mit deaktivierten Firewallregeln, die in $disabledRuleGroup 1 und $disabledRuleGroup 2 konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="72e50-112">The last command then creates a WAF configuration with firewall rules disabled as configured in $disabledRuleGroup1 and $disabledRuleGroup2.</span></span> <span data-ttu-id="72e50-113">Die neue WAF-Konfiguration wird in der $firewallConfig-Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="72e50-113">The new WAF configuration is stored in the $firewallConfig variable.</span></span>

## <span data-ttu-id="72e50-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="72e50-114">PARAMETERS</span></span>

### <span data-ttu-id="72e50-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72e50-115">-DefaultProfile</span></span>
<span data-ttu-id="72e50-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="72e50-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72e50-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="72e50-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="72e50-118">Die deaktivierten Regelgruppen.</span><span class="sxs-lookup"><span data-stu-id="72e50-118">The disabled rule groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup[]
Parameter Sets: (All)
Aliases: DisabledRuleGroups

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e50-119">-Aktiviert</span><span class="sxs-lookup"><span data-stu-id="72e50-119">-Enabled</span></span>
<span data-ttu-id="72e50-120">Gibt an, ob die WAF aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="72e50-120">Indicates whether the WAF is enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e50-121">– Ausschluss</span><span class="sxs-lookup"><span data-stu-id="72e50-121">-Exclusion</span></span>
<span data-ttu-id="72e50-122">Die Ausschlusslisten.</span><span class="sxs-lookup"><span data-stu-id="72e50-122">The exclusion lists.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallExclusion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e50-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="72e50-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="72e50-124">Maximale Dateiupload-Grenze in MB.</span><span class="sxs-lookup"><span data-stu-id="72e50-124">Max file upload limit in MB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e50-125">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="72e50-125">-FirewallMode</span></span>
<span data-ttu-id="72e50-126">Gibt den Web Application Firewall-Modus an.</span><span class="sxs-lookup"><span data-stu-id="72e50-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="72e50-127">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="72e50-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="72e50-128">Erkennung</span><span class="sxs-lookup"><span data-stu-id="72e50-128">Detection</span></span>
- <span data-ttu-id="72e50-129">Prävention</span><span class="sxs-lookup"><span data-stu-id="72e50-129">Prevention</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Detection, Prevention

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e50-130">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="72e50-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="72e50-131">Maximale Größe des Anforderungstexts in KB.</span><span class="sxs-lookup"><span data-stu-id="72e50-131">Max request body size in KB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e50-132">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="72e50-132">-RequestBodyCheck</span></span>
<span data-ttu-id="72e50-133">Ob der Anforderungstext aktiviert ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="72e50-133">Whether request body is checked or not.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e50-134">-Rulesettype</span><span class="sxs-lookup"><span data-stu-id="72e50-134">-RuleSetType</span></span>
<span data-ttu-id="72e50-135">Der Typ des Webanwendungs-Firewallregel-Regelsatzes.</span><span class="sxs-lookup"><span data-stu-id="72e50-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="72e50-136">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="72e50-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="72e50-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="72e50-137">OWASP</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OWASP

Required: False
Position: Named
Default value: OWASP
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e50-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="72e50-138">-RuleSetVersion</span></span>
<span data-ttu-id="72e50-139">Die Version des Regelsatztyps.</span><span class="sxs-lookup"><span data-stu-id="72e50-139">The version of the rule set type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 3.0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e50-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="72e50-140">-Confirm</span></span>
<span data-ttu-id="72e50-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="72e50-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e50-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72e50-142">-WhatIf</span></span>
<span data-ttu-id="72e50-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="72e50-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="72e50-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="72e50-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72e50-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72e50-145">CommonParameters</span></span>
<span data-ttu-id="72e50-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72e50-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72e50-147">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72e50-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72e50-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="72e50-148">INPUTS</span></span>

### <span data-ttu-id="72e50-149">Keine</span><span class="sxs-lookup"><span data-stu-id="72e50-149">None</span></span>

## <span data-ttu-id="72e50-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="72e50-150">OUTPUTS</span></span>

### <span data-ttu-id="72e50-151">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="72e50-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="72e50-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="72e50-152">NOTES</span></span>

## <span data-ttu-id="72e50-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="72e50-153">RELATED LINKS</span></span>

[<span data-ttu-id="72e50-154">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="72e50-154">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="72e50-155">Satz-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="72e50-155">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


