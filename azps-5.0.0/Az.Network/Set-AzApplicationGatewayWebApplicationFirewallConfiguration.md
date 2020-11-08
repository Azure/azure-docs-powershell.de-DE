---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 46FDE4D8-08E0-4465-8BF9-849A108628B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 9b5e618fc4b4be02614d872bfa5bcdabd2b0fec9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178147"
---
# <span data-ttu-id="36b6f-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="36b6f-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="36b6f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="36b6f-102">SYNOPSIS</span></span>
<span data-ttu-id="36b6f-103">Ändert die WAF-Konfiguration eines Anwendungs Gateways.</span><span class="sxs-lookup"><span data-stu-id="36b6f-103">Modifies the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="36b6f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="36b6f-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 -Enabled <Boolean> -FirewallMode <String> [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroup <PSApplicationGatewayFirewallDisabledRuleGroup[]>] [-RequestBodyCheck <Boolean>]
 [-MaxRequestBodySizeInKb <Int32>] [-FileUploadLimitInMb <Int32>]
 [-Exclusion <PSApplicationGatewayFirewallExclusion[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36b6f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="36b6f-105">DESCRIPTION</span></span>
<span data-ttu-id="36b6f-106">Das Cmdlet " **Satz-AzApplicationGatewayWebApplicationFirewallConfiguration** " ändert die WebApplication Firewall (WAF)-Konfiguration eines Anwendungs Gateways.</span><span class="sxs-lookup"><span data-stu-id="36b6f-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="36b6f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="36b6f-107">EXAMPLES</span></span>

### <span data-ttu-id="36b6f-108">Beispiel 1: Aktualisieren der Firewall-Konfiguration der Application Gateway-Webanwendung</span><span class="sxs-lookup"><span data-stu-id="36b6f-108">Example 1: Update the application gateway web application firewall configuration</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGw -Enabled $True -FirewallMode "Detection" -RuleSetType "OWASP" -RuleSetVersion "3.0"
```

<span data-ttu-id="36b6f-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab und speichert es dann in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="36b6f-109">The first command gets the application gateway named ApplicationGateway01 and then stores it in the $AppGw variable.</span></span>
<span data-ttu-id="36b6f-110">Der zweite Befehl aktiviert die Firewall-Konfiguration für das Anwendungsgateway, das in $AppGw gespeichert ist, und legt den Firewallmodus auf "Erkennung", rulesettype auf "OWASP" und RuleSetVersion auf "3,0" fest.</span><span class="sxs-lookup"><span data-stu-id="36b6f-110">The second command enables the firewall configuration for the application gateway stored in $AppGw and sets the firewall mode to "Detection", RuleSetType to "OWASP" and the RuleSetVersion to "3.0".</span></span>

## <span data-ttu-id="36b6f-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="36b6f-111">PARAMETERS</span></span>

### <span data-ttu-id="36b6f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="36b6f-112">-ApplicationGateway</span></span>
<span data-ttu-id="36b6f-113">Gibt ein Application Gateway-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="36b6f-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="36b6f-114">Sie können das Get-AzApplicationGateway-Cmdlet verwenden, um ein Application Gateway-Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="36b6f-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="36b6f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36b6f-115">-DefaultProfile</span></span>
<span data-ttu-id="36b6f-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="36b6f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36b6f-117">-DisabledRuleGroup</span><span class="sxs-lookup"><span data-stu-id="36b6f-117">-DisabledRuleGroup</span></span>
<span data-ttu-id="36b6f-118">Die deaktivierten Regelgruppen.</span><span class="sxs-lookup"><span data-stu-id="36b6f-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="36b6f-119">-Aktiviert</span><span class="sxs-lookup"><span data-stu-id="36b6f-119">-Enabled</span></span>
<span data-ttu-id="36b6f-120">Gibt an, ob die Webanwendungs Firewall aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="36b6f-120">Indicates whether the web application firewall is enabled.</span></span>

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

### <span data-ttu-id="36b6f-121">– Ausschluss</span><span class="sxs-lookup"><span data-stu-id="36b6f-121">-Exclusion</span></span>
<span data-ttu-id="36b6f-122">Die Ausschlusslisten.</span><span class="sxs-lookup"><span data-stu-id="36b6f-122">The exclusion lists.</span></span>

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

### <span data-ttu-id="36b6f-123">-FileUploadLimitInMb</span><span class="sxs-lookup"><span data-stu-id="36b6f-123">-FileUploadLimitInMb</span></span>
<span data-ttu-id="36b6f-124">Maximale Dateiupload-Grenze in MB.</span><span class="sxs-lookup"><span data-stu-id="36b6f-124">Max file upload limit in MB.</span></span>

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

### <span data-ttu-id="36b6f-125">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="36b6f-125">-FirewallMode</span></span>
<span data-ttu-id="36b6f-126">Gibt den Web Application Firewall-Modus an.</span><span class="sxs-lookup"><span data-stu-id="36b6f-126">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="36b6f-127">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="36b6f-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="36b6f-128">Erkennung</span><span class="sxs-lookup"><span data-stu-id="36b6f-128">Detection</span></span>
- <span data-ttu-id="36b6f-129">Prävention</span><span class="sxs-lookup"><span data-stu-id="36b6f-129">Prevention</span></span>

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

### <span data-ttu-id="36b6f-130">-MaxRequestBodySizeInKb</span><span class="sxs-lookup"><span data-stu-id="36b6f-130">-MaxRequestBodySizeInKb</span></span>
<span data-ttu-id="36b6f-131">Maximale Größe des Anforderungstexts in KB.</span><span class="sxs-lookup"><span data-stu-id="36b6f-131">Max request body size in KB.</span></span>

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

### <span data-ttu-id="36b6f-132">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="36b6f-132">-RequestBodyCheck</span></span>
<span data-ttu-id="36b6f-133">Ob der Anforderungstext aktiviert ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="36b6f-133">Whether request body is checked or not.</span></span>

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

### <span data-ttu-id="36b6f-134">-Rulesettype</span><span class="sxs-lookup"><span data-stu-id="36b6f-134">-RuleSetType</span></span>
<span data-ttu-id="36b6f-135">Der Typ des Webanwendungs-Firewallregel-Regelsatzes.</span><span class="sxs-lookup"><span data-stu-id="36b6f-135">The type of the web application firewall rule set.</span></span> <span data-ttu-id="36b6f-136">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="36b6f-136">The acceptable values for this parameter are:</span></span> 
- <span data-ttu-id="36b6f-137">OWASP</span><span class="sxs-lookup"><span data-stu-id="36b6f-137">OWASP</span></span>

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

### <span data-ttu-id="36b6f-138">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="36b6f-138">-RuleSetVersion</span></span>
<span data-ttu-id="36b6f-139">Die Version des Regelsatztyps.</span><span class="sxs-lookup"><span data-stu-id="36b6f-139">The version of the rule set type.</span></span>

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

### <span data-ttu-id="36b6f-140">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="36b6f-140">-Confirm</span></span>
<span data-ttu-id="36b6f-141">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="36b6f-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36b6f-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36b6f-142">-WhatIf</span></span>
<span data-ttu-id="36b6f-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="36b6f-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36b6f-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="36b6f-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36b6f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36b6f-145">CommonParameters</span></span>
<span data-ttu-id="36b6f-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36b6f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36b6f-147">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36b6f-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36b6f-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="36b6f-148">INPUTS</span></span>

### <span data-ttu-id="36b6f-149">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="36b6f-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="36b6f-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="36b6f-150">OUTPUTS</span></span>

### <span data-ttu-id="36b6f-151">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="36b6f-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="36b6f-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="36b6f-152">NOTES</span></span>

## <span data-ttu-id="36b6f-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="36b6f-153">RELATED LINKS</span></span>

[<span data-ttu-id="36b6f-154">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="36b6f-154">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="36b6f-155">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="36b6f-155">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="36b6f-156">Neu – AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="36b6f-156">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


