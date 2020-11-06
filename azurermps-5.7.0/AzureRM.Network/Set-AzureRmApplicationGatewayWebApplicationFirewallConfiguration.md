---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 46FDE4D8-08E0-4465-8BF9-849A108628B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 9da7a3d77c0a5f9b9dec44ee1224a66be79a1772
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481145"
---
# <span data-ttu-id="08bd7-101">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="08bd7-101">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="08bd7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="08bd7-102">SYNOPSIS</span></span>
<span data-ttu-id="08bd7-103">Ändert die WAF-Konfiguration eines Anwendungs Gateways.</span><span class="sxs-lookup"><span data-stu-id="08bd7-103">Modifies the WAF configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08bd7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="08bd7-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 -Enabled <Boolean> -FirewallMode <String> [-RuleSetType <String>] [-RuleSetVersion <String>]
 [-DisabledRuleGroups <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallDisabledRuleGroup]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08bd7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="08bd7-105">DESCRIPTION</span></span>
<span data-ttu-id="08bd7-106">Das Cmdlet " **Satz-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** " ändert die WebApplication Firewall (WAF)-Konfiguration eines Anwendungs Gateways.</span><span class="sxs-lookup"><span data-stu-id="08bd7-106">The **Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet modifies the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="08bd7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="08bd7-107">EXAMPLES</span></span>

### <span data-ttu-id="08bd7-108">Beispiel 1: Aktualisieren der Firewall-Konfiguration der Application Gateway-Webanwendung</span><span class="sxs-lookup"><span data-stu-id="08bd7-108">Example 1: Update the application gateway web application firewall configuration</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGw -Enabled $True -FirewallMode "Detection" -RuleSetType "OWASP" -RuleSetVersion "3.0"
```

<span data-ttu-id="08bd7-109">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab und speichert es dann in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="08bd7-109">The first command gets the application gateway named ApplicationGateway01 and then stores it in the $AppGw variable.</span></span>

<span data-ttu-id="08bd7-110">Der zweite Befehl aktiviert die Firewall-Konfiguration für das Anwendungsgateway, das in $AppGw gespeichert ist, und legt den Firewallmodus auf "Erkennung", rulesettype auf "OWASP" und RuleSetVersion auf "3,0" fest.</span><span class="sxs-lookup"><span data-stu-id="08bd7-110">The second command enables the firewall configuration for the application gateway stored in $AppGw and sets the firewall mode to "Detection", RuleSetType to "OWASP" and the RuleSetVersion to "3.0".</span></span>

## <span data-ttu-id="08bd7-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="08bd7-111">PARAMETERS</span></span>

### <span data-ttu-id="08bd7-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="08bd7-112">-ApplicationGateway</span></span>
<span data-ttu-id="08bd7-113">Gibt ein Application Gateway-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="08bd7-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="08bd7-114">Sie können das Get-AzureRmApplicationGateway-Cmdlet verwenden, um ein Application Gateway-Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="08bd7-114">You can use the Get-AzureRmApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="08bd7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08bd7-115">-DefaultProfile</span></span>
<span data-ttu-id="08bd7-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="08bd7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08bd7-117">-DisabledRuleGroups</span><span class="sxs-lookup"><span data-stu-id="08bd7-117">-DisabledRuleGroups</span></span>
<span data-ttu-id="08bd7-118">Die deaktivierten Regelgruppen.</span><span class="sxs-lookup"><span data-stu-id="08bd7-118">The disabled rule groups.</span></span>

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

### <span data-ttu-id="08bd7-119">-Aktiviert</span><span class="sxs-lookup"><span data-stu-id="08bd7-119">-Enabled</span></span>
<span data-ttu-id="08bd7-120">Gibt an, ob die Webanwendungs Firewall aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="08bd7-120">Indicates whether the web application firewall is enabled.</span></span>

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

### <span data-ttu-id="08bd7-121">-FirewallMode</span><span class="sxs-lookup"><span data-stu-id="08bd7-121">-FirewallMode</span></span>
<span data-ttu-id="08bd7-122">Gibt den Web Application Firewall-Modus an.</span><span class="sxs-lookup"><span data-stu-id="08bd7-122">Specifies the web application firewall mode.</span></span>
<span data-ttu-id="08bd7-123">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="08bd7-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="08bd7-124">Erkennung</span><span class="sxs-lookup"><span data-stu-id="08bd7-124">Detection</span></span>
- <span data-ttu-id="08bd7-125">Prävention</span><span class="sxs-lookup"><span data-stu-id="08bd7-125">Prevention</span></span>

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

### <span data-ttu-id="08bd7-126">-Rulesettype</span><span class="sxs-lookup"><span data-stu-id="08bd7-126">-RuleSetType</span></span>
<span data-ttu-id="08bd7-127">Der Typ des Webanwendungs-Firewallregel-Regelsatzes.</span><span class="sxs-lookup"><span data-stu-id="08bd7-127">The type of the web application firewall rule set.</span></span> <span data-ttu-id="08bd7-128">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="08bd7-128">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="08bd7-129">OWASP</span><span class="sxs-lookup"><span data-stu-id="08bd7-129">OWASP</span></span>

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

### <span data-ttu-id="08bd7-130">-RuleSetVersion</span><span class="sxs-lookup"><span data-stu-id="08bd7-130">-RuleSetVersion</span></span>
<span data-ttu-id="08bd7-131">Die Version des Regelsatztyps.</span><span class="sxs-lookup"><span data-stu-id="08bd7-131">The version of the rule set type.</span></span>
<span data-ttu-id="08bd7-132">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="08bd7-132">The acceptable values for this parameter are:</span></span> 

- <span data-ttu-id="08bd7-133">3,0</span><span class="sxs-lookup"><span data-stu-id="08bd7-133">3.0</span></span>
- <span data-ttu-id="08bd7-134">2.2.9</span><span class="sxs-lookup"><span data-stu-id="08bd7-134">2.2.9</span></span>

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

### <span data-ttu-id="08bd7-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="08bd7-135">-Confirm</span></span>
<span data-ttu-id="08bd7-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="08bd7-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08bd7-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08bd7-137">-WhatIf</span></span>
<span data-ttu-id="08bd7-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="08bd7-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="08bd7-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="08bd7-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08bd7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08bd7-140">CommonParameters</span></span>
<span data-ttu-id="08bd7-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08bd7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08bd7-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08bd7-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08bd7-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="08bd7-143">INPUTS</span></span>

### <span data-ttu-id="08bd7-144">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="08bd7-144">PSApplicationGateway</span></span>
<span data-ttu-id="08bd7-145">Der Parameter "ApplicationGateway" akzeptiert den Wert vom Typ "PSApplicationGateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="08bd7-145">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="08bd7-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="08bd7-146">OUTPUTS</span></span>

### <span data-ttu-id="08bd7-147">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="08bd7-147">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="08bd7-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="08bd7-148">NOTES</span></span>

## <span data-ttu-id="08bd7-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="08bd7-149">RELATED LINKS</span></span>

[<span data-ttu-id="08bd7-150">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="08bd7-150">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="08bd7-151">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="08bd7-151">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="08bd7-152">Neu – AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="08bd7-152">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)


