---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 46FDE4D8-08E0-4465-8BF9-849A108628B8
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 95d0e82609c2cb8bfcbbfcf57d1354d219da9f9a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941048"
---
# <span data-ttu-id="1aa47-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="1aa47-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="1aa47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1aa47-102">SYNOPSIS</span></span>
<span data-ttu-id="1aa47-103">Ändert die WAF-Konfiguration eines Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="1aa47-103">Modifies the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="1aa47-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1aa47-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 -Enabled <Boolean> -FirewallMode <String> [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <PSApplicationGatewayFirewallDisabledRuleGroup[]>] [-RequestBodyCheck <Boolean>]
 [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <PSApplicationGatewayFirewallExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1aa47-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1aa47-105">DESCRIPTION</span></span>
<span data-ttu-id="1aa47-106">Das **Cmdlet Set-AzApplicationGatewayWebApplicationFirewallConfiguration** ändert die Web Application Firewall (WAF)-Konfiguration eines Anwendungsgateways.</span><span class="sxs-lookup"><span data-stu-id="1aa47-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="1aa47-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1aa47-107">EXAMPLES</span></span>

### <span data-ttu-id="1aa47-108">Beispiel 1: Aktualisieren der Firewallkonfiguration des Anwendungsgateways</span><span class="sxs-lookup"><span data-stu-id="1aa47-108">Example 1: Update the application gateway web application firewall configuration</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGw -Enabled $True -FirewallMode "Detection" -RuleSetType "OWASP" -RuleSetVersion "3.0"
```

<span data-ttu-id="1aa47-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab und speichert es dann in der $AppGw-Variable.</span><span class="sxs-lookup"><span data-stu-id="1aa47-109">The first command gets the application gateway named ApplicationGateway01 and then stores it in the $AppGw variable.</span></span>
<span data-ttu-id="1aa47-110">Der zweite Befehl aktiviert die Firewallkonfiguration für das in $AppGw gespeicherte Anwendungsgateway und legt den Firewallmodus auf "Detection", RuleSetType auf "OWASP" und die RuleSetVersion auf "3.0" fest.</span><span class="sxs-lookup"><span data-stu-id="1aa47-110">The second command enables the firewall configuration for the application gateway stored in $AppGw and sets the firewall mode to "Detection", RuleSetType to "OWASP" and the RuleSetVersion to "3.0".</span></span>

## <span data-ttu-id="1aa47-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1aa47-111">PARAMETERS</span></span>

### <span data-ttu-id="1aa47-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1aa47-112">-ApplicationGateway</span></span>
<span data-ttu-id="1aa47-113">Gibt ein Anwendungsgatewayobjekt an.</span><span class="sxs-lookup"><span data-stu-id="1aa47-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="1aa47-114">Sie können das Get-AzApplicationGateway-Cmdlet verwenden, um ein Anwendungsgatewayobjekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1aa47-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1aa47-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1aa47-115">-DefaultProfile</span></span>
<span data-ttu-id="1aa47-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1aa47-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1aa47-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="1aa47-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="1aa47-118">Die deaktivierten Regelgruppen.</span><span class="sxs-lookup"><span data-stu-id="1aa47-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="1aa47-119">-Enabled</span><span class="sxs-lookup"><span data-stu-id="1aa47-119">-Enabled</span></span>
<span data-ttu-id="1aa47-120">Gibt an, ob die Webanwendungsfirewall aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1aa47-120">Indicates whether the web application firewall is enabled.</span></span>

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

### <span data-ttu-id="1aa47-121">-Ausschluss</span><span class="sxs-lookup"><span data-stu-id="1aa47-121">-Exclusion</span></span>
<span data-ttu-id="1aa47-122">Die Ausschlusslisten.</span><span class="sxs-lookup"><span data-stu-id="1aa47-122">The exclusion lists.</span></span>

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

### <span data-ttu-id="1aa47-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="1aa47-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="1aa47-124">Maximale Dateiuploadgrenze in MB.</span><span class="sxs-lookup"><span data-stu-id="1aa47-124">Max file upload limit in MB.</span></span>

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

### <span data-ttu-id="1aa47-125">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="1aa47-125">-FirewallMode</span></span>
<span data-ttu-id="1aa47-126">Gibt den Firewallmodus der Webanwendung an.</span><span class="sxs-lookup"><span data-stu-id="1aa47-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="1aa47-127">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="1aa47-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1aa47-128">Erkennung</span><span class="sxs-lookup"><span data-stu-id="1aa47-128">Detection</span></span>
- <span data-ttu-id="1aa47-129">Prävention</span><span class="sxs-lookup"><span data-stu-id="1aa47-129">Prevention</span></span>

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

### <span data-ttu-id="1aa47-130">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="1aa47-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="1aa47-131">Max. Anforderungstextgröße in KB.</span><span class="sxs-lookup"><span data-stu-id="1aa47-131">Max request body size in KB.</span></span>

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

### <span data-ttu-id="1aa47-132">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="1aa47-132">-RequestBodyCheck</span></span>
<span data-ttu-id="1aa47-133">Ob der Anforderungstext aktiviert ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="1aa47-133">Whether request body is checked or not.</span></span>

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

### <span data-ttu-id="1aa47-134">-RuleSetType</span><span class="sxs-lookup"><span data-stu-id="1aa47-134">-RuleSetType</span></span>
<span data-ttu-id="1aa47-135">Der Typ der Webanwendungsfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="1aa47-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="1aa47-136">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="1aa47-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="1aa47-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="1aa47-137">OWASP</span></span>

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

### <span data-ttu-id="1aa47-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="1aa47-138">-RuleSetVersion</span></span>
<span data-ttu-id="1aa47-139">Die Version des Regelsatztyps.</span><span class="sxs-lookup"><span data-stu-id="1aa47-139">The version of the rule set type.</span></span>

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

### <span data-ttu-id="1aa47-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1aa47-140">-Confirm</span></span>
<span data-ttu-id="1aa47-141">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1aa47-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1aa47-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1aa47-142">-WhatIf</span></span>
<span data-ttu-id="1aa47-143">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1aa47-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1aa47-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1aa47-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1aa47-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aa47-145">CommonParameters</span></span>
<span data-ttu-id="1aa47-146">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1aa47-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aa47-147">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1aa47-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aa47-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1aa47-148">INPUTS</span></span>

### <span data-ttu-id="1aa47-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1aa47-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1aa47-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1aa47-150">OUTPUTS</span></span>

### <span data-ttu-id="1aa47-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1aa47-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1aa47-152">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1aa47-152">NOTES</span></span>

## <span data-ttu-id="1aa47-153">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1aa47-153">RELATED LINKS</span></span>

[<span data-ttu-id="1aa47-154">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1aa47-154">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="1aa47-155">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="1aa47-155">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="1aa47-156">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="1aa47-156">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


