---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: b343ecbabd66f32be30f4aff1b0a44c7ddf186d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101935648"
---
# <span data-ttu-id="0e135-101">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0e135-101">New-AzApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="0e135-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e135-102">SYNOPSIS</span></span>
<span data-ttu-id="0e135-103">Erstellt eine Anwendungsgatewaypfadregel.</span><span class="sxs-lookup"><span data-stu-id="0e135-103">Creates an application gateway path rule.</span></span>

## <span data-ttu-id="0e135-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0e135-104">SYNTAX</span></span>

### <span data-ttu-id="0e135-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0e135-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e135-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="0e135-106">SetByResource</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e135-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0e135-107">DESCRIPTION</span></span>
<span data-ttu-id="0e135-108">Das **Cmdlet New-AzApplicationGatewayPathRuleConfig** erstellt eine Anwendungsgatewaypfadregel.</span><span class="sxs-lookup"><span data-stu-id="0e135-108">The **New-AzApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="0e135-109">Von diesem Cmdlet erstellte Regeln können einer Sammlung von Konfigurationseinstellungen für die URL-Pfadzuordnung hinzugefügt und dann einem Gateway zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="0e135-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>
<span data-ttu-id="0e135-110">Einstellungen für die Pfadzuordnungskonfiguration werden beim Lastenausgleich des Anwendungsgateways verwendet.</span><span class="sxs-lookup"><span data-stu-id="0e135-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="0e135-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0e135-111">EXAMPLES</span></span>

### <span data-ttu-id="0e135-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0e135-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="0e135-113">Diese Befehle erstellen eine neue Anwendungsgatewaypfadregel und verwenden dann das **Cmdlet Add-AzApplicationGatewayUrlPathMapConfig,** um diese Regel einem Anwendungsgateway zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="0e135-113">These commands create a new application gateway path rule and then use the **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="0e135-114">Dazu erstellt der erste Befehl einen Objektverweis auf das Gateway ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="0e135-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="0e135-115">Dieser Objektverweis wird in einer Variablen namens $Gateway.</span><span class="sxs-lookup"><span data-stu-id="0e135-115">This object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="0e135-116">Die nächsten beiden Befehle erstellen einen Back-End-Adresspool und ein Back-End-HTTP-Einstellungsobjekt. Diese Objekte (gespeichert in den Variablen $AddressPool und $HttpSettings) sind erforderlich, um ein Pfadregelobjekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0e135-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>
<span data-ttu-id="0e135-117">Der vierte Befehl erstellt das Pfadregelobjekt und wird in einer Variablen namens $PathRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="0e135-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>
<span data-ttu-id="0e135-118">Der fünfte Befehl verwendet **Add-AzApplicationGatewayUrlPathMapConfig,** um die Konfigurationseinstellungen und die neue Pfadregel, die in diesen Einstellungen enthalten sind, zu ContosoApplicationGateway hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="0e135-118">The fifth command uses **Add-AzApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

### <span data-ttu-id="0e135-119">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0e135-119">Example 2</span></span>
```
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings -FirewallPolicy $firewallPolicy
```

<span data-ttu-id="0e135-120">Mit diesem Befehl wird eine Pfadregel mit dem Namen als "basis", Pfaden als "/base", Back-EndAddressPool als $AddressPool, Back-EndHttpSettings as $HttpSettings und FirewallPolicy als $firewallPolicy.ngs und der neuen Pfadregel erstellt, die in diesen Einstellungen zu ContosoApplicationGateway enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="0e135-120">These command creates a path-rule with the Name as "base", Paths as "/base", BackendAddressPool as $AddressPool, BackendHttpSettings as $HttpSettings and FirewallPolicy as $firewallPolicy.ngs and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="0e135-121">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0e135-121">PARAMETERS</span></span>

### <span data-ttu-id="0e135-122">-Back-EndAddressPool</span><span class="sxs-lookup"><span data-stu-id="0e135-122">-BackendAddressPool</span></span>
<span data-ttu-id="0e135-123">Gibt einen Objektverweis auf eine Sammlung von Einstellungen für den Back-End-Adresspool an, die den Konfigurationseinstellungen für Gatewaypfadregeln hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0e135-123">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="0e135-124">Sie können diesen Objektverweis mit dem cmdlet New-AzApplicationGatewayBackendAddressPool und der folgenden Syntax erstellen: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span><span class="sxs-lookup"><span data-stu-id="0e135-124">You can create this object reference by using the New-AzApplicationGatewayBackendAddressPool cmdlet and syntax similar to this: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span></span>
<span data-ttu-id="0e135-125">Der vorhergehende Befehl fügt dem Adresspool zwei IP-Adressen (192.16.1.1 und 192.168.1.2) hinzu.</span><span class="sxs-lookup"><span data-stu-id="0e135-125">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="0e135-126">Beachten Sie, dass die IP-Adresse in Anführungszeichen eingeschlossen und durch Kommas getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="0e135-126">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>
<span data-ttu-id="0e135-127">Die resultierende Variable, $AddressPool, kann dann als Parameterwert für den *DefaultBackendAddressPool-Parameter verwendet* werden.</span><span class="sxs-lookup"><span data-stu-id="0e135-127">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="0e135-128">Der Back-End-Adresspool stellt die IP-Adressen auf den Back-End-Servern dar.</span><span class="sxs-lookup"><span data-stu-id="0e135-128">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="0e135-129">Diese IP-Adressen sollten entweder zum Subnetz des virtuellen Netzwerks gehören oder öffentliche IP-Adressen sein.</span><span class="sxs-lookup"><span data-stu-id="0e135-129">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="0e135-130">Wenn Sie diesen Parameter verwenden, können Sie den *Parameter DefaultBackendAddressPoolId* nicht im gleichen Befehl verwenden.</span><span class="sxs-lookup"><span data-stu-id="0e135-130">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e135-131">-Back-EndAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="0e135-131">-BackendAddressPoolId</span></span>
<span data-ttu-id="0e135-132">Gibt die ID eines vorhandenen Back-End-Adresspools an, der den Konfigurationseinstellungen der Gatewaypfadregel hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="0e135-132">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="0e135-133">Adresspool-IDs können über das cmdlet Get-AzApplicationGatewayBackendAddressPool zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0e135-133">Address pool IDs can be returned by using the Get-AzApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="0e135-134">Nachdem Sie über die ID verfügen, können Sie den *Parameter DefaultBackendAddressPoolId* anstelle des *DefaultBackendAddressPool-Parameters* verwenden.</span><span class="sxs-lookup"><span data-stu-id="0e135-134">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="0e135-135">Beispiel: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backAddressPools/ContosoAddressPool" Der Back-End-Adresspool stellt die IP-Adressen auf den Back-End-Servern dar.</span><span class="sxs-lookup"><span data-stu-id="0e135-135">For instance: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="0e135-136">Diese IP-Adressen sollten entweder zum Subnetz des virtuellen Netzwerks gehören oder öffentliche IP-Adressen sein.</span><span class="sxs-lookup"><span data-stu-id="0e135-136">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e135-137">-Back-EndHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0e135-137">-BackendHttpSettings</span></span>
<span data-ttu-id="0e135-138">Gibt einen Objektverweis auf eine Sammlung von Back-End-HTTP-Einstellungen an, die den Konfigurationseinstellungen der Gatewaypfadregel hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0e135-138">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="0e135-139">Sie können diesen Objektverweis mithilfe des New-AzApplicationGatewayBackendHttpSettings-Cmdlets und der folgenden Syntax erstellen: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" Die resultierende Variable, $HttpSettings kann dann als Parameterwert für den *DefaultBackendAddressPool-Parameter* verwendet werden: -DefaultBackendHttpSettings $HttpSettings Die Back-End-HTTP-Einstellungen konfigurieren Eigenschaften wie Port, Protokoll und cookiebasierte Affinität für einen Back-End-Pool.</span><span class="sxs-lookup"><span data-stu-id="0e135-139">You can create this object reference by using the New-AzApplicationGatewayBackendHttpSettings cmdlet and syntax similar to this: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter: -DefaultBackendHttpSettings $HttpSettings The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="0e135-140">Wenn Sie diesen Parameter verwenden, können Sie den *Parameter DefaultBackendHttpSettingsId* nicht im gleichen Befehl verwenden.</span><span class="sxs-lookup"><span data-stu-id="0e135-140">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e135-141">-Back-EndHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="0e135-141">-BackendHttpSettingsId</span></span>
<span data-ttu-id="0e135-142">Gibt die ID einer vorhandenen HTTP-Back-End-Einstellungssammlung an, die den Konfigurationseinstellungen der Gatewaypfadregel hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="0e135-142">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="0e135-143">HTTP-Einstellungs-IDs können mithilfe des cmdlets Get-AzApplicationGatewayBackendHttpSettings zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0e135-143">HTTP setting IDs can be returned by using the Get-AzApplicationGatewayBackendHttpSettings cmdlet.</span></span>
<span data-ttu-id="0e135-144">Nachdem Sie über die ID verfügen, können Sie den *Parameter DefaultBackendHttpSettingsId* anstelle des *Parameters DefaultBackendHttpSettings* verwenden.</span><span class="sxs-lookup"><span data-stu-id="0e135-144">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="0e135-145">Beispiel: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backHttpSettingsCollection/ContosoHttpSettings" Die Backend-HTTP-Einstellungen konfigurieren Eigenschaften wie Port, und cookiebasierte Affinität für einen Back-End-Pool.</span><span class="sxs-lookup"><span data-stu-id="0e135-145">For instance: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="0e135-146">Wenn Sie diesen Parameter verwenden, können Sie den *Parameter DefaultBackendHttpSettings* nicht im gleichen Befehl verwenden.</span><span class="sxs-lookup"><span data-stu-id="0e135-146">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e135-147">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="0e135-147">-FirewallPolicy</span></span>
<span data-ttu-id="0e135-148">Gibt den Objektverweis auf eine Firewallrichtlinie der obersten Ebene an.</span><span class="sxs-lookup"><span data-stu-id="0e135-148">Specifies the object reference to a top-level firewall policy.</span></span> <span data-ttu-id="0e135-149">Der Objektverweis kann mithilfe des cmdlets New-AzApplicationGatewayWebApplicationFirewallPolicy werden.</span><span class="sxs-lookup"><span data-stu-id="0e135-149">The object reference can be created by using New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span>
<span data-ttu-id="0e135-150">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" Eine Firewallrichtlinie, die mit dem obigen Befehllet erstellt wurde, kann auf pfadregelebene verwiesen werden.</span><span class="sxs-lookup"><span data-stu-id="0e135-150">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be referred at a path-rule level.</span></span> <span data-ttu-id="0e135-151">Der obige Befehl würde eine Standardrichtlinieneinstellungen und verwaltete Regeln erstellen.</span><span class="sxs-lookup"><span data-stu-id="0e135-151">he above command would create a default policy settings and managed rules.</span></span>
<span data-ttu-id="0e135-152">Anstelle der Standardwerte können Benutzer "PolicySettings", "ManagedRules" New-AzApplicationGatewayFirewallPolicySettings und New-AzApplicationGatewayFirewallPolicyManagedRules angeben.</span><span class="sxs-lookup"><span data-stu-id="0e135-152">Instead of the default values, users can specify PolicySettings, ManagedRules by using New-AzApplicationGatewayFirewallPolicySettings and New-AzApplicationGatewayFirewallPolicyManagedRules respectively.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e135-153">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="0e135-153">-FirewallPolicyId</span></span>
<span data-ttu-id="0e135-154">Gibt die ID einer vorhandenen Webanwendungsfirewallressource der obersten Ebene an.</span><span class="sxs-lookup"><span data-stu-id="0e135-154">Specifies the ID of an existing top-level web application firewall resource.</span></span>
<span data-ttu-id="0e135-155">Firewallrichtlinien-IDs können über das cmdlet Get-AzApplicationGatewayWebApplicationFirewallPolicy zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0e135-155">Firewall policy IDs can be returned by using the Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span> <span data-ttu-id="0e135-156">Nachdem wir die ID haben, können Sie den *Parameter FirewallPolicyId* anstelle des *FirewallPolicy-Parameters* verwenden.</span><span class="sxs-lookup"><span data-stu-id="0e135-156">After we have the ID you can use *FirewallPolicyId* parameter instead of *FirewallPolicy* parameter.</span></span>
<span data-ttu-id="0e135-157">Beispiel: -FirewallPolicyId "/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName> "</span><span class="sxs-lookup"><span data-stu-id="0e135-157">For instance: -FirewallPolicyId  "/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/<firewallPolicyName>"</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e135-158">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e135-158">-DefaultProfile</span></span>
<span data-ttu-id="0e135-159">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0e135-159">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e135-160">-Name</span><span class="sxs-lookup"><span data-stu-id="0e135-160">-Name</span></span>
<span data-ttu-id="0e135-161">Gibt den Namen der Pfadregelkonfiguration an, die von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="0e135-161">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="0e135-162">-Paths</span><span class="sxs-lookup"><span data-stu-id="0e135-162">-Paths</span></span>
<span data-ttu-id="0e135-163">Gibt eine oder mehrere Pfadregeln für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="0e135-163">Specifies one or more application gateway path rules.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e135-164">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e135-164">-RedirectConfiguration</span></span>
<span data-ttu-id="0e135-165">RedirectConfiguration des Anwendungsgateways</span><span class="sxs-lookup"><span data-stu-id="0e135-165">Application gateway RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e135-166">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="0e135-166">-RedirectConfigurationId</span></span>
<span data-ttu-id="0e135-167">ID des Anwendungsgateways RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e135-167">ID of the application gateway RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e135-168">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0e135-168">-RewriteRuleSet</span></span>
<span data-ttu-id="0e135-169">Anwendungsgateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0e135-169">Application gateway RewriteRuleSet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e135-170">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="0e135-170">-RewriteRuleSetId</span></span>
<span data-ttu-id="0e135-171">ID des Anwendungsgateways RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0e135-171">ID of the application gateway RewriteRuleSet</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e135-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e135-172">CommonParameters</span></span>
<span data-ttu-id="0e135-173">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e135-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e135-174">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e135-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e135-175">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0e135-175">INPUTS</span></span>

### <span data-ttu-id="0e135-176">Keine</span><span class="sxs-lookup"><span data-stu-id="0e135-176">None</span></span>

## <span data-ttu-id="0e135-177">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0e135-177">OUTPUTS</span></span>

### <span data-ttu-id="0e135-178">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span><span class="sxs-lookup"><span data-stu-id="0e135-178">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span></span>

## <span data-ttu-id="0e135-179">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0e135-179">NOTES</span></span>

## <span data-ttu-id="0e135-180">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0e135-180">RELATED LINKS</span></span>

[<span data-ttu-id="0e135-181">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0e135-181">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="0e135-182">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0e135-182">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="0e135-183">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0e135-183">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="0e135-184">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0e135-184">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="0e135-185">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="0e135-185">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="0e135-186">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0e135-186">New-AzApplicationGatewayPathRuleConfig</span></span>](./New-AzApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="0e135-187">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0e135-187">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="0e135-188">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0e135-188">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="0e135-189">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0e135-189">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


