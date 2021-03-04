---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 76DB6AF5-BF6F-436C-8500-626468F84466
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 7d13febefe06ed1c290a0f95cbfda39dea353426
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931576"
---
# <span data-ttu-id="92406-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="92406-101">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="92406-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92406-102">SYNOPSIS</span></span>
<span data-ttu-id="92406-103">Erstellt eine WAF-Konfiguration für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="92406-103">Creates a WAF configuration for an application gateway.</span></span>

## <span data-ttu-id="92406-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="92406-104">SYNTAX</span></span>

```
New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled <Boolean> -FirewallMode <String>
 [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <PSApplicationGatewayFirewallDisabledRuleGroup[]>] [-RequestBodyCheck <Boolean>]
 [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <PSApplicationGatewayFirewallExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92406-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="92406-105">DESCRIPTION</span></span>
<span data-ttu-id="92406-106">Das **Cmdlet New-AzApplicationGatewayWebApplicationFirewallConfiguration** erstellt eine WAF-Konfiguration (Web Application Firewall) für ein Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="92406-106">The **New-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet creates a web application firewall (WAF) configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="92406-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="92406-107">EXAMPLES</span></span>

### <span data-ttu-id="92406-108">Beispiel 1: Erstellen einer Webanwendungsfirewallkonfiguration für ein Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="92406-108">Example 1: Create a web application firewall configuration for an application gateway</span></span>
```
PS C:\> $disabledRuleGroup1 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-942-APPLICATION-ATTACK-SQLI" -Rules 942130,942140
PS C:\> $disabledRuleGroup2 = New-AzApplicationGatewayFirewallDisabledRuleGroupConfig -RuleGroupName "REQUEST-921-PROTOCOL-ATTACK"
PS C:\> $firewallConfig = New-AzApplicationGatewayWebApplicationFirewallConfiguration -Enabled $true -FirewallMode "Prevention" -RuleSetType "OWASP" -RuleSetVersion "3.0" -DisabledRuleGroups $disabledRuleGroup1,$disabledRuleGroup2
```

<span data-ttu-id="92406-109">Mit dem ersten Befehl wird eine neue deaktivierte Regelgruppenkonfiguration für die Regelgruppe mit dem Namen "REQUEST-942-APPLICATION-ATTACK-SQLI" erstellt, bei der Regel 942130 und Regel 942140 deaktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="92406-109">The first command creates a new disabled rule group configuration for the rule group named "REQUEST-942-APPLICATION-ATTACK-SQLI" with rule 942130 and rule 942140 being disabled.</span></span>
<span data-ttu-id="92406-110">Mit dem zweiten Befehl wird eine weitere deaktivierte Regelgruppenkonfiguration für eine Regelgruppe namens "REQUEST-921-PROTOCOL-ATTACK" erstellt.</span><span class="sxs-lookup"><span data-stu-id="92406-110">The second command creates another disabled rule group configuration for a rule group named "REQUEST-921-PROTOCOL-ATTACK".</span></span> <span data-ttu-id="92406-111">Es werden keine Regeln speziell übergeben, und daher werden alle Regeln der Regelgruppe deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="92406-111">No rules are specifically passed and thus all rules of the rule group will be disabled.</span></span>
<span data-ttu-id="92406-112">Mit dem letzten Befehl wird dann eine WAF-Konfiguration mit Firewallregeln erstellt, die wie in $disabledRuleGroup 1 und $disabledRuleGroup 2 konfiguriert deaktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="92406-112">The last command then creates a WAF configuration with firewall rules disabled as configured in $disabledRuleGroup1 and $disabledRuleGroup2.</span></span> <span data-ttu-id="92406-113">Die neue WAF-Konfiguration wird in der $firewallConfig gespeichert.</span><span class="sxs-lookup"><span data-stu-id="92406-113">The new WAF configuration is stored in the $firewallConfig variable.</span></span>

## <span data-ttu-id="92406-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="92406-114">PARAMETERS</span></span>

### <span data-ttu-id="92406-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92406-115">-DefaultProfile</span></span>
<span data-ttu-id="92406-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="92406-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92406-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="92406-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="92406-118">Die deaktivierten Regelgruppen.</span><span class="sxs-lookup"><span data-stu-id="92406-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="92406-119">-Enabled</span><span class="sxs-lookup"><span data-stu-id="92406-119">-Enabled</span></span>
<span data-ttu-id="92406-120">Gibt an, ob die WAF aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="92406-120">Indicates whether the WAF is enabled.</span></span>

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

### <span data-ttu-id="92406-121">-Ausschluss</span><span class="sxs-lookup"><span data-stu-id="92406-121">-Exclusion</span></span>
<span data-ttu-id="92406-122">Die Ausschlusslisten.</span><span class="sxs-lookup"><span data-stu-id="92406-122">The exclusion lists.</span></span>

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

### <span data-ttu-id="92406-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="92406-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="92406-124">Maximale Dateiuploadgrenze in MB.</span><span class="sxs-lookup"><span data-stu-id="92406-124">Max file upload limit in MB.</span></span>

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

### <span data-ttu-id="92406-125">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="92406-125">-FirewallMode</span></span>
<span data-ttu-id="92406-126">Gibt den Firewallmodus der Webanwendung an.</span><span class="sxs-lookup"><span data-stu-id="92406-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="92406-127">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="92406-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="92406-128">Erkennung</span><span class="sxs-lookup"><span data-stu-id="92406-128">Detection</span></span>
- <span data-ttu-id="92406-129">Prävention</span><span class="sxs-lookup"><span data-stu-id="92406-129">Prevention</span></span>

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

### <span data-ttu-id="92406-130">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="92406-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="92406-131">Max. Anforderungstextgröße in KB.</span><span class="sxs-lookup"><span data-stu-id="92406-131">Max request body size in KB.</span></span>

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

### <span data-ttu-id="92406-132">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="92406-132">-RequestBodyCheck</span></span>
<span data-ttu-id="92406-133">Ob der Anforderungstext aktiviert ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="92406-133">Whether request body is checked or not.</span></span>

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

### <span data-ttu-id="92406-134">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="92406-134">-RuleSetType</span></span>
<span data-ttu-id="92406-135">Der Typ der Webanwendungsfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="92406-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="92406-136">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="92406-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="92406-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="92406-137">OWASP</span></span>

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

### <span data-ttu-id="92406-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="92406-138">-RuleSetVersion</span></span>
<span data-ttu-id="92406-139">Die Version des Regelsatztyps.</span><span class="sxs-lookup"><span data-stu-id="92406-139">The version of the rule set type.</span></span>

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

### <span data-ttu-id="92406-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="92406-140">-Confirm</span></span>
<span data-ttu-id="92406-141">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="92406-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92406-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92406-142">-WhatIf</span></span>
<span data-ttu-id="92406-143">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="92406-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="92406-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="92406-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92406-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92406-145">CommonParameters</span></span>
<span data-ttu-id="92406-146">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92406-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92406-147">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92406-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92406-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="92406-148">INPUTS</span></span>

### <span data-ttu-id="92406-149">Keine</span><span class="sxs-lookup"><span data-stu-id="92406-149">None</span></span>

## <span data-ttu-id="92406-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="92406-150">OUTPUTS</span></span>

### <span data-ttu-id="92406-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="92406-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="92406-152">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="92406-152">NOTES</span></span>

## <span data-ttu-id="92406-153">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="92406-153">RELATED LINKS</span></span>

[<span data-ttu-id="92406-154">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="92406-154">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="92406-155">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="92406-155">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


