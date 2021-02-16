---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: 94fbc1e9a4ae8b7befe6961a9648174770458583
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400211"
---
# <span data-ttu-id="9e041-101">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9e041-101">New-AzApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="9e041-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e041-102">SYNOPSIS</span></span>
<span data-ttu-id="9e041-103">Erstellt eine Anwendungsgatewaypfadregel.</span><span class="sxs-lookup"><span data-stu-id="9e041-103">Creates an application gateway path rule.</span></span>

## <span data-ttu-id="9e041-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9e041-104">SYNTAX</span></span>

### <span data-ttu-id="9e041-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9e041-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e041-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9e041-106">SetByResource</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e041-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9e041-107">DESCRIPTION</span></span>
<span data-ttu-id="9e041-108">Das **Cmdlet "New-AzApplicationGatewayPathRuleConfig"** erstellt eine Anwendungsgatewaypfadregel.</span><span class="sxs-lookup"><span data-stu-id="9e041-108">The **New-AzApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="9e041-109">Von diesem Cmdlet erstellte Regeln können einer Sammlung von Konfigurationseinstellungen für die URL-Pfadzuordnung hinzugefügt und dann einem Gateway zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="9e041-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>
<span data-ttu-id="9e041-110">Die Konfigurationseinstellungen der Pfadzuordnung werden beim Lastenausgleich des Anwendungsgateways verwendet.</span><span class="sxs-lookup"><span data-stu-id="9e041-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="9e041-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9e041-111">EXAMPLES</span></span>

### <span data-ttu-id="9e041-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9e041-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="9e041-113">Diese Befehle erstellen eine neue Regel für den Anwendungsgatewaypfad und verwenden dann das **Cmdlet "Add-AzApplicationGatewayUrlPathMapConfig",** um die Regel einem Anwendungsgateway zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="9e041-113">These commands create a new application gateway path rule and then use the **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="9e041-114">Dazu erstellt der erste Befehl einen Objektverweis auf das Gateway "ContosoApplicationGateway".</span><span class="sxs-lookup"><span data-stu-id="9e041-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="9e041-115">Dieser Objektverweis wird in einer Variablen mit dem Namen $Gateway.</span><span class="sxs-lookup"><span data-stu-id="9e041-115">This object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="9e041-116">Mit den nächsten beiden Befehlen werden ein Back-End-Adresspool und ein #A0 für #A1 erstellt. diese Objekte (in den Variablen $AddressPool und $HttpSettings gespeichert) benötigt, um ein Pfadregelobjekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9e041-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>
<span data-ttu-id="9e041-117">Der vierte Befehl erstellt das Pfadregelobjekt und wird in einer Variablen namens "$PathRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="9e041-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>
<span data-ttu-id="9e041-118">Der fünfte Befehl verwendet **"Add-AzApplicationGatewayUrlPathMapConfig",** um die Konfigurationseinstellungen und die neue Pfadregel, die in diesen Einstellungen enthalten sind, zu "ContosoApplicationGateway" hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="9e041-118">The fifth command uses **Add-AzApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="9e041-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e041-119">PARAMETERS</span></span>

### <span data-ttu-id="9e041-120">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9e041-120">-BackendAddressPool</span></span>
<span data-ttu-id="9e041-121">Gibt einen Objektverweis auf eine Sammlung von Einstellungen für den Back-End-Adresspool an, die den Konfigurationseinstellungen der Gatewaypfadregeln hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9e041-121">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="9e041-122">Sie können diesen Objektverweis mithilfe des #New-AzApplicationGatewayBackendAddressPool und einer ähnlichen Syntax erstellen: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span><span class="sxs-lookup"><span data-stu-id="9e041-122">You can create this object reference by using the New-AzApplicationGatewayBackendAddressPool cmdlet and syntax similar to this: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span></span>
<span data-ttu-id="9e041-123">Der vorherige Befehl fügt dem Adresspool zwei IP-Adressen (192.16.1.1 und 192.168.1.2) hinzu.</span><span class="sxs-lookup"><span data-stu-id="9e041-123">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="9e041-124">Beachten Sie, dass die IP-Adresse in Anführungszeichen eingeschlossen und durch Kommas getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="9e041-124">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>
<span data-ttu-id="9e041-125">Die resultierende Variable ($AddressPool) kann dann als Parameterwert für den Parameter *"DefaultBackendAddressPool" verwendet* werden.</span><span class="sxs-lookup"><span data-stu-id="9e041-125">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="9e041-126">Der Back-End-Adresspool stellt die IP-Adressen auf den Back-End-Servern dar.</span><span class="sxs-lookup"><span data-stu-id="9e041-126">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="9e041-127">Diese IP-Adressen sollten entweder zum Subnetz des virtuellen Netzwerks gehören oder öffentliche IP-Adressen sein.</span><span class="sxs-lookup"><span data-stu-id="9e041-127">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="9e041-128">Wenn Sie diesen Parameter verwenden, können Sie den Parameter *"DefaultBackendAddressPoolId"* nicht im gleichen Befehl verwenden.</span><span class="sxs-lookup"><span data-stu-id="9e041-128">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

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

### <span data-ttu-id="9e041-129">-Back-EndAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="9e041-129">-BackendAddressPoolId</span></span>
<span data-ttu-id="9e041-130">Gibt die ID eines vorhandenen Back-End-Adresspools an, der den Konfigurationseinstellungen der Gatewaypfadregel hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="9e041-130">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="9e041-131">Adresspool-IDs können mit dem cmdlet Get-AzApplicationGatewayBackendAddressPool zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9e041-131">Address pool IDs can be returned by using the Get-AzApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="9e041-132">Nachdem Sie über die ID verfügen, können Sie den Parameter *"DefaultBackendAddressPoolId"* anstelle des Parameters *"DefaultBackendAddressPool"* verwenden.</span><span class="sxs-lookup"><span data-stu-id="9e041-132">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="9e041-133">Beispiel: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" Der Back-End-Adresspool stellt die IP-Adressen auf den Back-End-Servern dar.</span><span class="sxs-lookup"><span data-stu-id="9e041-133">For instance: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="9e041-134">Diese IP-Adressen sollten entweder zum Subnetz des virtuellen Netzwerks gehören oder öffentliche IP-Adressen sein.</span><span class="sxs-lookup"><span data-stu-id="9e041-134">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

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

### <span data-ttu-id="9e041-135">-Back-EndHttpSettings</span><span class="sxs-lookup"><span data-stu-id="9e041-135">-BackendHttpSettings</span></span>
<span data-ttu-id="9e041-136">Gibt einen Objektverweis auf eine Sammlung von HTTP-Back-End-Einstellungen an, die den Konfigurationseinstellungen der Gatewaypfadregel hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9e041-136">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="9e041-137">Sie können diesen Objektverweis mithilfe des Cmdlets New-AzApplicationGatewayBackendHttpSettings und einer ähnlichen Syntax erstellen: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" Die resultierende Variable, $HttpSettings kann dann als Parameterwert für den *Parameter "DefaultBackendAddressPool"* verwendet werden: -DefaultBackendHttpSettings $HttpSettings Die Back-End-HTTP-Einstellungen konfigurieren Eigenschaften wie Port, Protokoll und cookiebasierte Affinität für einen Back-End-Pool.</span><span class="sxs-lookup"><span data-stu-id="9e041-137">You can create this object reference by using the New-AzApplicationGatewayBackendHttpSettings cmdlet and syntax similar to this: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter: -DefaultBackendHttpSettings $HttpSettings The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="9e041-138">Wenn Sie diesen Parameter verwenden, können Sie den Parameter *"DefaultBackendHttpSettingsId"* nicht im gleichen Befehl verwenden.</span><span class="sxs-lookup"><span data-stu-id="9e041-138">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

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

### <span data-ttu-id="9e041-139">-Back-EndHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="9e041-139">-BackendHttpSettingsId</span></span>
<span data-ttu-id="9e041-140">Gibt die ID einer vorhandenen HTTP-Back-End-Einstellungssammlung an, die den Konfigurationseinstellungen der Gatewaypfadregel hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="9e041-140">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="9e041-141">HTTP-Einstellungs-IDs können mit dem cmdlet Get-AzApplicationGatewayBackendHttpSettings zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9e041-141">HTTP setting IDs can be returned by using the Get-AzApplicationGatewayBackendHttpSettings cmdlet.</span></span>
<span data-ttu-id="9e041-142">Nachdem Sie die ID erhalten haben, können Sie anstelle des Parameters *"DefaultBackendHttpSettingsId"* den Parameter *"DefaultBackendHttpSettings"* verwenden.</span><span class="sxs-lookup"><span data-stu-id="9e041-142">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="9e041-143">Beispiel: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backHttpSettingsCollection/ContosoHttpSettings" Die Back-End-HTTP-Einstellungen konfigurieren Eigenschaften wie Port, und cookiebasierte Affinität für einen Back-End-Pool.</span><span class="sxs-lookup"><span data-stu-id="9e041-143">For instance: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="9e041-144">Wenn Sie diesen Parameter verwenden, können Sie den Parameter *"DefaultBackendHttpSettings"* nicht in demselben Befehl verwenden.</span><span class="sxs-lookup"><span data-stu-id="9e041-144">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

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

### <span data-ttu-id="9e041-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e041-145">-DefaultProfile</span></span>
<span data-ttu-id="9e041-146">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9e041-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e041-147">-Name</span><span class="sxs-lookup"><span data-stu-id="9e041-147">-Name</span></span>
<span data-ttu-id="9e041-148">Gibt den Namen der Pfadregelkonfiguration an, die von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="9e041-148">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="9e041-149">-Paths</span><span class="sxs-lookup"><span data-stu-id="9e041-149">-Paths</span></span>
<span data-ttu-id="9e041-150">Gibt eine oder mehrere Anwendungsgatewaypfadregeln an.</span><span class="sxs-lookup"><span data-stu-id="9e041-150">Specifies one or more application gateway path rules.</span></span>

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

### <span data-ttu-id="9e041-151">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="9e041-151">-RedirectConfiguration</span></span>
<span data-ttu-id="9e041-152">Anwendungsgateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="9e041-152">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="9e041-153">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="9e041-153">-RedirectConfigurationId</span></span>
<span data-ttu-id="9e041-154">ID des Anwendungsgateways RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="9e041-154">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="9e041-155">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9e041-155">-RewriteRuleSet</span></span>
<span data-ttu-id="9e041-156">Application gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="9e041-156">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="9e041-157">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="9e041-157">-RewriteRuleSetId</span></span>
<span data-ttu-id="9e041-158">ID des Anwendungsgateways "RewriteRuleSet"</span><span class="sxs-lookup"><span data-stu-id="9e041-158">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="9e041-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e041-159">CommonParameters</span></span>
<span data-ttu-id="9e041-160">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e041-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e041-161">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e041-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e041-162">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9e041-162">INPUTS</span></span>

### <span data-ttu-id="9e041-163">Keine</span><span class="sxs-lookup"><span data-stu-id="9e041-163">None</span></span>

## <span data-ttu-id="9e041-164">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9e041-164">OUTPUTS</span></span>

### <span data-ttu-id="9e041-165">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span><span class="sxs-lookup"><span data-stu-id="9e041-165">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span></span>

## <span data-ttu-id="9e041-166">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9e041-166">NOTES</span></span>

## <span data-ttu-id="9e041-167">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9e041-167">RELATED LINKS</span></span>

[<span data-ttu-id="9e041-168">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9e041-168">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="9e041-169">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9e041-169">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="9e041-170">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9e041-170">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="9e041-171">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="9e041-171">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)


[<span data-ttu-id="9e041-172">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9e041-172">New-AzApplicationGatewayPathRuleConfig</span></span>](./New-AzApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="9e041-173">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9e041-173">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="9e041-174">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9e041-174">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="9e041-175">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="9e041-175">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


