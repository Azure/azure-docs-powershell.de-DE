---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 46FDE4D8-08E0-4465-8BF9-849A108628B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: bf4a87ebae55329e4594d11559fda0aee9047cbc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843652"
---
# <span data-ttu-id="7bff3-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="7bff3-101">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="7bff3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7bff3-102">SYNOPSIS</span></span>
<span data-ttu-id="7bff3-103">Ändert die WAF-Konfiguration eines Anwendungs Gateways.</span><span class="sxs-lookup"><span data-stu-id="7bff3-103">Modifies the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="7bff3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7bff3-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 -Enabled <Boolean> -FirewallMode <String> [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroups <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bff3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7bff3-105">DESCRIPTION</span></span>
<span data-ttu-id="7bff3-106">Das Cmdlet " **Satz-AzApplicationGatewayWebApplicationFirewallConfiguration** " ändert die WebApplication Firewall (WAF)-Konfiguration eines Anwendungs Gateways.</span><span class="sxs-lookup"><span data-stu-id="7bff3-106">The **Set-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="7bff3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7bff3-107">EXAMPLES</span></span>

### <span data-ttu-id="7bff3-108">Beispiel 1: Aktualisieren der Firewall-Konfiguration der Application Gateway-Webanwendung</span><span class="sxs-lookup"><span data-stu-id="7bff3-108">Example 1: Update the application gateway web application firewall configuration</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Set-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGw -Enabled $True -FirewallMode "Detection" -RuleSetType "OWASP" -RuleSetVersion "3.0"
```

<span data-ttu-id="7bff3-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab und speichert es dann in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="7bff3-109">The first command gets the application gateway named ApplicationGateway01 and then stores it in the $AppGw variable.</span></span>

<span data-ttu-id="7bff3-110">Der zweite Befehl aktiviert die Firewall-Konfiguration für das Anwendungsgateway, das in $AppGw gespeichert ist, und legt den Firewallmodus auf "Erkennung", rulesettype auf "OWASP" und RuleSetVersion auf "3,0" fest.</span><span class="sxs-lookup"><span data-stu-id="7bff3-110">The second command enables the firewall configuration for the application gateway stored in $AppGw and sets the firewall mode to "Detection", RuleSetType to "OWASP" and the RuleSetVersion to "3.0".</span></span>

## <span data-ttu-id="7bff3-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="7bff3-111">PARAMETERS</span></span>

### <span data-ttu-id="7bff3-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7bff3-112">-ApplicationGateway</span></span>
<span data-ttu-id="7bff3-113">Gibt ein Application Gateway-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="7bff3-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="7bff3-114">Sie können das Get-AzApplicationGateway-Cmdlet verwenden, um ein Application Gateway-Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7bff3-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7bff3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bff3-115">-DefaultProfile</span></span>
<span data-ttu-id="7bff3-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7bff3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bff3-117">-DisabledRuleGroups</span><span class="sxs-lookup"><span data-stu-id="7bff3-117">-DisabledRuleGroups</span></span>
<span data-ttu-id="7bff3-118">Die deaktivierten Regelgruppen.</span><span class="sxs-lookup"><span data-stu-id="7bff3-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="7bff3-119">-Aktiviert</span><span class="sxs-lookup"><span data-stu-id="7bff3-119">-Enabled</span></span>
<span data-ttu-id="7bff3-120">Gibt an, ob die Webanwendungs Firewall aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7bff3-120">Indicates whether the web application firewall is enabled.</span></span>

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

### <span data-ttu-id="7bff3-121">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="7bff3-121">-FirewallMode</span></span>
<span data-ttu-id="7bff3-122">Gibt den Web Application Firewall-Modus an.</span><span class="sxs-lookup"><span data-stu-id="7bff3-122">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="7bff3-123">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7bff3-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7bff3-124">Erkennung</span><span class="sxs-lookup"><span data-stu-id="7bff3-124">Detection</span></span>
- <span data-ttu-id="7bff3-125">Prävention</span><span class="sxs-lookup"><span data-stu-id="7bff3-125">Prevention</span></span>

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

### <span data-ttu-id="7bff3-126">-Rulesettype</span><span class="sxs-lookup"><span data-stu-id="7bff3-126">-RuleSetType</span></span>
<span data-ttu-id="7bff3-127">Der Typ des Webanwendungs-Firewallregel-Regelsatzes.</span><span class="sxs-lookup"><span data-stu-id="7bff3-127">The type of the web application firewall rule set.</span></span> <span data-ttu-id="7bff3-128">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7bff3-128">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="7bff3-129">OWASP</span><span class="sxs-lookup"><span data-stu-id="7bff3-129">OWASP</span></span>

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

### <span data-ttu-id="7bff3-130">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="7bff3-130">-RuleSetVersion</span></span>
<span data-ttu-id="7bff3-131">Die Version des Regelsatztyps.</span><span class="sxs-lookup"><span data-stu-id="7bff3-131">The version of the rule set type.</span></span>
<span data-ttu-id="7bff3-132">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7bff3-132">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="7bff3-133">3,0</span><span class="sxs-lookup"><span data-stu-id="7bff3-133">3.0</span></span>
- <span data-ttu-id="7bff3-134">2.2.9</span><span class="sxs-lookup"><span data-stu-id="7bff3-134">2.2.9</span></span>

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

### <span data-ttu-id="7bff3-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7bff3-135">-Confirm</span></span>
<span data-ttu-id="7bff3-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7bff3-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bff3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bff3-137">-WhatIf</span></span>
<span data-ttu-id="7bff3-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7bff3-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7bff3-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7bff3-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bff3-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bff3-140">CommonParameters</span></span>
<span data-ttu-id="7bff3-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bff3-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bff3-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bff3-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bff3-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7bff3-143">INPUTS</span></span>

### <span data-ttu-id="7bff3-144">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7bff3-144">PSApplicationGateway</span></span>
<span data-ttu-id="7bff3-145">Der Parameter "ApplicationGateway" akzeptiert den Wert vom Typ "PSApplicationGateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="7bff3-145">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="7bff3-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7bff3-146">OUTPUTS</span></span>

### <span data-ttu-id="7bff3-147">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7bff3-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7bff3-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="7bff3-148">NOTES</span></span>

## <span data-ttu-id="7bff3-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7bff3-149">RELATED LINKS</span></span>

[<span data-ttu-id="7bff3-150">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7bff3-150">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="7bff3-151">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="7bff3-151">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="7bff3-152">Neu – AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="7bff3-152">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


