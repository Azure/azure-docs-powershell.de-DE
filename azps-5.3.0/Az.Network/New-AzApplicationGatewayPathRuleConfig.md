---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: c36cb832034535f13cbcb49805531c64ee906c60
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379404"
---
# <span data-ttu-id="470c6-101">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="470c6-101">New-AzApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="470c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="470c6-102">SYNOPSIS</span></span>
<span data-ttu-id="470c6-103">Erstellt eine Anwendungsgatewaypfadregel.</span><span class="sxs-lookup"><span data-stu-id="470c6-103">Creates an application gateway path rule.</span></span>

## <span data-ttu-id="470c6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="470c6-104">SYNTAX</span></span>

### <span data-ttu-id="470c6-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="470c6-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-FirewallPolicyId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="470c6-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="470c6-106">SetByResource</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="470c6-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="470c6-107">DESCRIPTION</span></span>
<span data-ttu-id="470c6-108">Das **Cmdlet "New-AzApplicationGatewayPathRuleConfig"** erstellt eine Anwendungsgatewaypfadregel.</span><span class="sxs-lookup"><span data-stu-id="470c6-108">The **New-AzApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="470c6-109">Von diesem Cmdlet erstellte Regeln können einer Sammlung von Konfigurationseinstellungen für die URL-Pfadzuordnung hinzugefügt und dann einem Gateway zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="470c6-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>
<span data-ttu-id="470c6-110">Die Konfigurationseinstellungen der Pfadzuordnung werden beim Lastenausgleich des Anwendungsgateways verwendet.</span><span class="sxs-lookup"><span data-stu-id="470c6-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="470c6-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="470c6-111">EXAMPLES</span></span>

### <span data-ttu-id="470c6-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="470c6-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="470c6-113">Mit diesen Befehlen wird eine neue Pfadregel für das Anwendungsgateway erstellt und dann das **Cmdlet "Add-AzApplicationGatewayUrlPathMapConfig"** verwendet, um die Regel einem Anwendungsgateway zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="470c6-113">These commands create a new application gateway path rule and then use the **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="470c6-114">Dazu erstellt der erste Befehl einen Objektverweis auf das Gateway "ContosoApplicationGateway".</span><span class="sxs-lookup"><span data-stu-id="470c6-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="470c6-115">Dieser Objektverweis wird in einer Variablen mit dem Namen $Gateway.</span><span class="sxs-lookup"><span data-stu-id="470c6-115">This object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="470c6-116">Mit den nächsten beiden Befehlen werden ein Back-End-Adresspool und ein #A0 für #A1 erstellt. diese Objekte (in den Variablen $AddressPool und $HttpSettings) benötigt, um ein Pfadregelobjekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="470c6-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>
<span data-ttu-id="470c6-117">Der vierte Befehl erstellt das Pfadregelobjekt und wird in einer Variablen namens $PathRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="470c6-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>
<span data-ttu-id="470c6-118">Der fünfte Befehl verwendet **"Add-AzApplicationGatewayUrlPathMapConfig",** um die Konfigurationseinstellungen und die neue Pfadregel, die in diesen Einstellungen enthalten sind, zu "ContosoApplicationGateway" hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="470c6-118">The fifth command uses **Add-AzApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

### <span data-ttu-id="470c6-119">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="470c6-119">Example 2</span></span>
```
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings -FirewallPolicy $firewallPolicy
```

<span data-ttu-id="470c6-120">Dieser Befehl erstellt eine Pfadregel mit dem Namen als "basis", Pfaden als "/base", Back-EndAddressPool als $AddressPool, Back-EndHttpSettings als $HttpSettings und FirewallPolicy als $firewallPolicy.ngs und der neuen Pfadregel, die in diesen Einstellungen zu ContosoApplicationGateway enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="470c6-120">These command creates a path-rule with the Name as "base", Paths as "/base", BackendAddressPool as $AddressPool, BackendHttpSettings as $HttpSettings and FirewallPolicy as $firewallPolicy.ngs and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="470c6-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="470c6-121">PARAMETERS</span></span>

### <span data-ttu-id="470c6-122">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="470c6-122">-BackendAddressPool</span></span>
<span data-ttu-id="470c6-123">Gibt einen Objektverweis auf eine Sammlung von Einstellungen für den Back-End-Adresspool an, die den Konfigurationseinstellungen der Gatewaypfadregeln hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="470c6-123">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="470c6-124">Sie können diesen Objektverweis erstellen, indem Sie das cmdlet New-AzApplicationGatewayBackendAddressPool und eine ähnliche Syntax wie die folgende verwenden: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span><span class="sxs-lookup"><span data-stu-id="470c6-124">You can create this object reference by using the New-AzApplicationGatewayBackendAddressPool cmdlet and syntax similar to this: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span></span>
<span data-ttu-id="470c6-125">Der vorherige Befehl fügt dem Adresspool zwei IP-Adressen (192.16.1.1 und 192.168.1.2) hinzu.</span><span class="sxs-lookup"><span data-stu-id="470c6-125">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="470c6-126">Beachten Sie, dass die IP-Adresse in Anführungszeichen eingeschlossen und durch Kommas getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="470c6-126">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>
<span data-ttu-id="470c6-127">Die resultierende Variable ($AddressPool) kann dann als Parameterwert für den Parameter *"DefaultBackendAddressPool" verwendet* werden.</span><span class="sxs-lookup"><span data-stu-id="470c6-127">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="470c6-128">Der Back-End-Adresspool stellt die IP-Adressen auf den Back-End-Servern dar.</span><span class="sxs-lookup"><span data-stu-id="470c6-128">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="470c6-129">Diese IP-Adressen sollten entweder zum Subnetz des virtuellen Netzwerks gehören oder öffentliche IP-Adressen sein.</span><span class="sxs-lookup"><span data-stu-id="470c6-129">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="470c6-130">Wenn Sie diesen Parameter verwenden, können Sie den Parameter *"DefaultBackendAddressPoolId"* nicht im gleichen Befehl verwenden.</span><span class="sxs-lookup"><span data-stu-id="470c6-130">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

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

### <span data-ttu-id="470c6-131">-Back-EndAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="470c6-131">-BackendAddressPoolId</span></span>
<span data-ttu-id="470c6-132">Gibt die ID eines vorhandenen Back-End-Adresspools an, der den Konfigurationseinstellungen der Gatewaypfadregel hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="470c6-132">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="470c6-133">Adresspool-IDs können mit dem cmdlet Get-AzApplicationGatewayBackendAddressPool zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="470c6-133">Address pool IDs can be returned by using the Get-AzApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="470c6-134">Nachdem Sie die ID erhalten haben, können Sie den Parameter *"DefaultBackendAddressPoolId"* anstelle des Parameters *"DefaultBackendAddressPool"* verwenden.</span><span class="sxs-lookup"><span data-stu-id="470c6-134">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="470c6-135">Beispiel: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" Der Back-End-Adresspool stellt die IP-Adressen auf den Back-End-Servern dar.</span><span class="sxs-lookup"><span data-stu-id="470c6-135">For instance: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="470c6-136">Diese IP-Adressen sollten entweder zum Subnetz des virtuellen Netzwerks gehören oder öffentliche IP-Adressen sein.</span><span class="sxs-lookup"><span data-stu-id="470c6-136">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

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

### <span data-ttu-id="470c6-137">-Back-EndHttpSettings</span><span class="sxs-lookup"><span data-stu-id="470c6-137">-BackendHttpSettings</span></span>
<span data-ttu-id="470c6-138">Gibt einen Objektverweis auf eine Sammlung von HTTP-Back-End-Einstellungen an, die den Konfigurationseinstellungen der Gatewaypfadregel hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="470c6-138">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="470c6-139">Sie können diesen Objektverweis mithilfe des Cmdlets New-AzApplicationGatewayBackendHttpSettings und einer ähnlichen Syntax erstellen: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" Die resultierende Variable, $HttpSettings kann dann als Parameterwert für den *Parameter "DefaultBackendAddressPool"* verwendet werden: -DefaultBackendHttpSettings $HttpSettings Die Back-End-HTTP-Einstellungen konfigurieren Eigenschaften wie Port, Protokoll und cookiebasierte Affinität für einen Back-End-Pool.</span><span class="sxs-lookup"><span data-stu-id="470c6-139">You can create this object reference by using the New-AzApplicationGatewayBackendHttpSettings cmdlet and syntax similar to this: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter: -DefaultBackendHttpSettings $HttpSettings The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="470c6-140">Wenn Sie diesen Parameter verwenden, können Sie den Parameter *"DefaultBackendHttpSettingsId"* nicht im gleichen Befehl verwenden.</span><span class="sxs-lookup"><span data-stu-id="470c6-140">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

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

### <span data-ttu-id="470c6-141">-Back-EndHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="470c6-141">-BackendHttpSettingsId</span></span>
<span data-ttu-id="470c6-142">Gibt die ID einer vorhandenen HTTP-Back-End-Einstellungssammlung an, die den Konfigurationseinstellungen der Gatewaypfadregel hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="470c6-142">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="470c6-143">HTTP-Einstellungs-IDs können mit dem cmdlet Get-AzApplicationGatewayBackendHttpSettings zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="470c6-143">HTTP setting IDs can be returned by using the Get-AzApplicationGatewayBackendHttpSettings cmdlet.</span></span>
<span data-ttu-id="470c6-144">Nachdem Sie die ID erhalten haben, können Sie anstelle des Parameters *"DefaultBackendHttpSettingsId"* den Parameter *"DefaultBackendHttpSettings"* verwenden.</span><span class="sxs-lookup"><span data-stu-id="470c6-144">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="470c6-145">Beispiel: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backHttpSettingsCollection/ContosoHttpSettings" Die Back-End-HTTP-Einstellungen konfigurieren Eigenschaften wie Port, und cookiebasierte Affinität für einen Back-End-Pool.</span><span class="sxs-lookup"><span data-stu-id="470c6-145">For instance: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="470c6-146">Wenn Sie diesen Parameter verwenden, können Sie den Parameter *"DefaultBackendHttpSettings"* nicht in demselben Befehl verwenden.</span><span class="sxs-lookup"><span data-stu-id="470c6-146">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

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

### <span data-ttu-id="470c6-147">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="470c6-147">-FirewallPolicy</span></span>
<span data-ttu-id="470c6-148">Gibt den Objektverweis auf eine Firewallrichtlinie der obersten Ebene an.</span><span class="sxs-lookup"><span data-stu-id="470c6-148">Specifies the object reference to a top-level firewall policy.</span></span> <span data-ttu-id="470c6-149">Der Objektverweis kann mithilfe eines cmdlets New-AzApplicationGatewayWebApplicationFirewallPolicy werden.</span><span class="sxs-lookup"><span data-stu-id="470c6-149">The object reference can be created by using New-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span>
<span data-ttu-id="470c6-150">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" Auf eine Firewallrichtlinie, die mit dem obigen Befehlslet erstellt wurde, kann auf Pfadregelebene verwiesen werden.</span><span class="sxs-lookup"><span data-stu-id="470c6-150">$firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name "wafPolicy1" -ResourceGroup "rgName" A firewall policy created using the above commandlet can be referred at a path-rule level.</span></span> <span data-ttu-id="470c6-151">Der oben aufgeführte Befehl würde standardmäßige Richtlinieneinstellungen und verwaltete Regeln erstellen.</span><span class="sxs-lookup"><span data-stu-id="470c6-151">he above command would create a default policy settings and managed rules.</span></span>
<span data-ttu-id="470c6-152">Statt der Standardwerte können Benutzer "PolicySettings", "ManagedRules" New-AzApplicationGatewayFirewallPolicySettings und New-AzApplicationGatewayFirewallPolicyManagedRules angeben.</span><span class="sxs-lookup"><span data-stu-id="470c6-152">Instead of the default values, users can specify PolicySettings, ManagedRules by using New-AzApplicationGatewayFirewallPolicySettings and New-AzApplicationGatewayFirewallPolicyManagedRules respectively.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="470c6-153">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="470c6-153">-FirewallPolicyId</span></span>
<span data-ttu-id="470c6-154">Gibt die ID einer vorhandenen Webanwendungsfirewallressource der obersten Ebene an.</span><span class="sxs-lookup"><span data-stu-id="470c6-154">Specifies the ID of an existing top-level web application firewall resource.</span></span>
<span data-ttu-id="470c6-155">Firewallrichtlinien-IDs können mit dem cmdlet Get-AzApplicationGatewayWebApplicationFirewallPolicy zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="470c6-155">Firewall policy IDs can be returned by using the Get-AzApplicationGatewayWebApplicationFirewallPolicy cmdlet.</span></span> <span data-ttu-id="470c6-156">Nachdem wir die ID haben, können Sie den Parameter *"FirewallPolicyId"* anstelle des Parameters *"FirewallPolicy"* verwenden.</span><span class="sxs-lookup"><span data-stu-id="470c6-156">After we have the ID you can use *FirewallPolicyId* parameter instead of *FirewallPolicy* parameter.</span></span>
<span data-ttu-id="470c6-157">Beispiel: -FirewallPolicyId "/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/ <firewallPolicyName> "</span><span class="sxs-lookup"><span data-stu-id="470c6-157">For instance: -FirewallPolicyId  "/subscriptions/<subscription-id>/resourceGroups/<resource-group-id>/providers/Microsoft.Network/ApplicationGatewayWebApplicationFirewallPolicies/<firewallPolicyName>"</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="470c6-158">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="470c6-158">-DefaultProfile</span></span>
<span data-ttu-id="470c6-159">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="470c6-159">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="470c6-160">-Name</span><span class="sxs-lookup"><span data-stu-id="470c6-160">-Name</span></span>
<span data-ttu-id="470c6-161">Gibt den Namen der Pfadregelkonfiguration an, die von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="470c6-161">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="470c6-162">-Paths</span><span class="sxs-lookup"><span data-stu-id="470c6-162">-Paths</span></span>
<span data-ttu-id="470c6-163">Gibt eine oder mehrere Regeln für den Anwendungsgatewaypfad an.</span><span class="sxs-lookup"><span data-stu-id="470c6-163">Specifies one or more application gateway path rules.</span></span>

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

### <span data-ttu-id="470c6-164">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="470c6-164">-RedirectConfiguration</span></span>
<span data-ttu-id="470c6-165">Anwendungsgateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="470c6-165">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="470c6-166">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="470c6-166">-RedirectConfigurationId</span></span>
<span data-ttu-id="470c6-167">ID des Anwendungsgateways RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="470c6-167">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="470c6-168">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="470c6-168">-RewriteRuleSet</span></span>
<span data-ttu-id="470c6-169">Application gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="470c6-169">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="470c6-170">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="470c6-170">-RewriteRuleSetId</span></span>
<span data-ttu-id="470c6-171">ID des Anwendungsgateways "RewriteRuleSet"</span><span class="sxs-lookup"><span data-stu-id="470c6-171">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="470c6-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="470c6-172">CommonParameters</span></span>
<span data-ttu-id="470c6-173">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="470c6-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="470c6-174">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="470c6-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="470c6-175">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="470c6-175">INPUTS</span></span>

### <span data-ttu-id="470c6-176">Keine</span><span class="sxs-lookup"><span data-stu-id="470c6-176">None</span></span>

## <span data-ttu-id="470c6-177">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="470c6-177">OUTPUTS</span></span>

### <span data-ttu-id="470c6-178">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span><span class="sxs-lookup"><span data-stu-id="470c6-178">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span></span>

## <span data-ttu-id="470c6-179">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="470c6-179">NOTES</span></span>

## <span data-ttu-id="470c6-180">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="470c6-180">RELATED LINKS</span></span>

[<span data-ttu-id="470c6-181">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="470c6-181">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="470c6-182">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="470c6-182">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="470c6-183">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="470c6-183">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="470c6-184">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="470c6-184">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="470c6-185">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="470c6-185">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="470c6-186">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="470c6-186">New-AzApplicationGatewayPathRuleConfig</span></span>](./New-AzApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="470c6-187">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="470c6-187">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="470c6-188">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="470c6-188">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="470c6-189">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="470c6-189">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


