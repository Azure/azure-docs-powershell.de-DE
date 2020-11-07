---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: 82940003bbd40cfb15d1f109fbdd1b820d6bd647
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822184"
---
# <span data-ttu-id="c1f09-101">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c1f09-101">New-AzApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="c1f09-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c1f09-102">SYNOPSIS</span></span>
<span data-ttu-id="c1f09-103">Erstellt eine Anwendungsgateway-Pfadregel.</span><span class="sxs-lookup"><span data-stu-id="c1f09-103">Creates an application gateway path rule.</span></span>

## <span data-ttu-id="c1f09-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1f09-104">SYNTAX</span></span>

### <span data-ttu-id="c1f09-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c1f09-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1f09-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c1f09-106">SetByResource</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1f09-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c1f09-107">DESCRIPTION</span></span>
<span data-ttu-id="c1f09-108">Das Cmdlet **New-AzApplicationGatewayPathRuleConfig** erstellt eine Pfadregel für das Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="c1f09-108">The **New-AzApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="c1f09-109">Von diesem Cmdlet erstellte Regeln können einer Sammlung von URL-Pfad Zuordnungs Konfigurationseinstellungen hinzugefügt und dann einem Gateway zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="c1f09-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>
<span data-ttu-id="c1f09-110">Konfigurationseinstellungen für Pfad Zuordnungen werden im Lastenausgleich des Anwendungs Gateways verwendet.</span><span class="sxs-lookup"><span data-stu-id="c1f09-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="c1f09-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c1f09-111">EXAMPLES</span></span>

### <span data-ttu-id="c1f09-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c1f09-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="c1f09-113">Mit diesen Befehlen wird eine neue Anwendungsgateway-Pfadregel erstellt, und dann wird das Cmdlet **Add-AzApplicationGatewayUrlPathMapConfig** verwendet, um die Regel einem Anwendungsgateway zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="c1f09-113">These commands create a new application gateway path rule and then use the **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="c1f09-114">Dazu erstellt der erste Befehl einen Objektverweis auf das Gateway-ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="c1f09-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="c1f09-115">Dieser Objektverweis wird in einer Variablen mit dem Namen $Gateway gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c1f09-115">This object reference is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="c1f09-116">Mit den nächsten beiden Befehlen wird ein Back-End-Adresspool und ein Back-End-HTTP-Einstellungsobjekt erstellt. Diese Objekte (in den Variablen $AddressPool und $HttpSettings gespeichert) werden benötigt, um ein Pfadregel-Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c1f09-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>
<span data-ttu-id="c1f09-117">Der vierte Befehl erstellt das Pfadregel-Objekt und wird in einer Variablen mit dem Namen $PathRuleConfig gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c1f09-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>
<span data-ttu-id="c1f09-118">Der fünfte Befehl verwendet **Add-AzApplicationGatewayUrlPathMapConfig** , um die Konfigurationseinstellungen und die neue Pfadregel, die in diesen Einstellungen enthalten ist, ContosoApplicationGateway hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="c1f09-118">The fifth command uses **Add-AzApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="c1f09-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1f09-119">PARAMETERS</span></span>

### <span data-ttu-id="c1f09-120">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c1f09-120">-BackendAddressPool</span></span>
<span data-ttu-id="c1f09-121">Gibt einen Objektverweis auf eine Sammlung von Einstellungen des Back-End-Adresspools an, die den Konfigurationseinstellungen für Gateway-Pfadregeln hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c1f09-121">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="c1f09-122">Sie können diesen Objektverweis mithilfe des New-AzApplicationGatewayBackendAddressPool-Cmdlets und der Syntax wie folgt erstellen: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span><span class="sxs-lookup"><span data-stu-id="c1f09-122">You can create this object reference by using the New-AzApplicationGatewayBackendAddressPool cmdlet and syntax similar to this: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`</span></span>
<span data-ttu-id="c1f09-123">Der vorhergehende Befehl fügt dem Adresspool zwei IP-Adressen (192.16.1.1 und 192.168.1.2) hinzu.</span><span class="sxs-lookup"><span data-stu-id="c1f09-123">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="c1f09-124">Beachten Sie, dass die IP-Adresse in Anführungszeichen eingeschlossen und durch Kommas getrennt wird.</span><span class="sxs-lookup"><span data-stu-id="c1f09-124">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>
<span data-ttu-id="c1f09-125">Die resultierende Variable $AddressPool kann dann als Parameterwert für den *DefaultBackendAddressPool* -Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c1f09-125">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="c1f09-126">Der Back-End-Adresspool stellt die IP-Adressen auf den Back-End-Servern dar.</span><span class="sxs-lookup"><span data-stu-id="c1f09-126">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="c1f09-127">Diese IP-Adressen sollten entweder zum Subnetz des virtuellen Netzwerks gehören oder öffentliche IP-Adressen sein.</span><span class="sxs-lookup"><span data-stu-id="c1f09-127">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="c1f09-128">Wenn Sie diesen Parameter verwenden, können Sie den *DefaultBackendAddressPoolId* -Parameter nicht im gleichen Befehl verwenden.</span><span class="sxs-lookup"><span data-stu-id="c1f09-128">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

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

### <span data-ttu-id="c1f09-129">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="c1f09-129">-BackendAddressPoolId</span></span>
<span data-ttu-id="c1f09-130">Gibt die ID eines vorhandenen Back-End-Adresspools an, der den Konfigurationseinstellungen für Gateway-Pfad Regel hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="c1f09-130">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="c1f09-131">Adresspool-IDs können mithilfe des Get-AzApplicationGatewayBackendAddressPool-Cmdlets zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c1f09-131">Address pool IDs can be returned by using the Get-AzApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="c1f09-132">Nachdem Sie die ID haben, können Sie den *DefaultBackendAddressPoolId* -Parameter anstelle des *DefaultBackendAddressPool* -Parameters verwenden.</span><span class="sxs-lookup"><span data-stu-id="c1f09-132">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="c1f09-133">Beispiel:-DefaultBackendAddressPoolId "/Subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-RG/Providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" der Back-End-Adresspool stellt die IP-Adressen auf den Back-End-Servern dar.</span><span class="sxs-lookup"><span data-stu-id="c1f09-133">For instance: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool" The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="c1f09-134">Diese IP-Adressen sollten entweder zum Subnetz des virtuellen Netzwerks gehören oder öffentliche IP-Adressen sein.</span><span class="sxs-lookup"><span data-stu-id="c1f09-134">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

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

### <span data-ttu-id="c1f09-135">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c1f09-135">-BackendHttpSettings</span></span>
<span data-ttu-id="c1f09-136">Gibt einen Objektverweis auf eine Sammlung von Back-End-HTTP-Einstellungen an, die den Konfigurationseinstellungen für Gateway-Pfad Regel hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c1f09-136">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="c1f09-137">Sie können diesen Objektverweis mithilfe des New-AzApplicationGatewayBackendHttpSettings-Cmdlets und der Syntax wie folgt erstellen: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings-Name "ContosoHttpSettings"-Port 80-Protokoll "http"-CookieBasedAffinity "disabled" die resultierende Variable, $HttpSettings, kann dann als Parameterwert für den *DefaultBackendAddressPool* -Parameter verwendet werden:-DefaultBackendHttpSettings $HttpSettings die Back-End-HTTP-Einstellungen konfigurieren Eigenschaften wie Port, Protokoll und Cookie-basierte Affinität für einen Back-End-Pool.</span><span class="sxs-lookup"><span data-stu-id="c1f09-137">You can create this object reference by using the New-AzApplicationGatewayBackendHttpSettings cmdlet and syntax similar to this: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter: -DefaultBackendHttpSettings $HttpSettings The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="c1f09-138">Wenn Sie diesen Parameter verwenden, können Sie den *DefaultBackendHttpSettingsId* -Parameter nicht im gleichen Befehl verwenden.</span><span class="sxs-lookup"><span data-stu-id="c1f09-138">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

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

### <span data-ttu-id="c1f09-139">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="c1f09-139">-BackendHttpSettingsId</span></span>
<span data-ttu-id="c1f09-140">Gibt die ID einer vorhandenen Back-End-HTTP-Einstellungs Sammlung an, die den Konfigurationseinstellungen für Gateway-Pfad Regel hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="c1f09-140">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="c1f09-141">HTTP-Einstellungs-IDs können mithilfe des Get-AzApplicationGatewayBackendHttpSettings-Cmdlets zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c1f09-141">HTTP setting IDs can be returned by using the Get-AzApplicationGatewayBackendHttpSettings cmdlet.</span></span>
<span data-ttu-id="c1f09-142">Nachdem Sie die ID haben, können Sie den *DefaultBackendHttpSettingsId* -Parameter anstelle des *DefaultBackendHttpSettings* -Parameters verwenden.</span><span class="sxs-lookup"><span data-stu-id="c1f09-142">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="c1f09-143">Beispiel:-DefaultBackendSettings-ID "/Subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-RG/Providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" die HTTP-Back-End-Einstellungen konfigurieren Eigenschaften wie Port-, Protokoll-und Cookie-basierter Affinität für einen Back-End-Pool.</span><span class="sxs-lookup"><span data-stu-id="c1f09-143">For instance: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="c1f09-144">Wenn Sie diesen Parameter verwenden, können Sie den *DefaultBackendHttpSettings* -Parameter nicht im gleichen Befehl verwenden.</span><span class="sxs-lookup"><span data-stu-id="c1f09-144">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

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

### <span data-ttu-id="c1f09-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1f09-145">-DefaultProfile</span></span>
<span data-ttu-id="c1f09-146">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c1f09-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1f09-147">-Name</span><span class="sxs-lookup"><span data-stu-id="c1f09-147">-Name</span></span>
<span data-ttu-id="c1f09-148">Gibt den Namen der vom Cmdlet erstellten Pfad Regelkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="c1f09-148">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c1f09-149">-Pfade</span><span class="sxs-lookup"><span data-stu-id="c1f09-149">-Paths</span></span>
<span data-ttu-id="c1f09-150">Gibt mindestens eine Application Gateway Path-Regel an.</span><span class="sxs-lookup"><span data-stu-id="c1f09-150">Specifies one or more application gateway path rules.</span></span>

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

### <span data-ttu-id="c1f09-151">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1f09-151">-RedirectConfiguration</span></span>
<span data-ttu-id="c1f09-152">Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1f09-152">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="c1f09-153">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c1f09-153">-RedirectConfigurationId</span></span>
<span data-ttu-id="c1f09-154">ID des Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1f09-154">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="c1f09-155">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c1f09-155">-RewriteRuleSet</span></span>
<span data-ttu-id="c1f09-156">Application Gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c1f09-156">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="c1f09-157">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="c1f09-157">-RewriteRuleSetId</span></span>
<span data-ttu-id="c1f09-158">ID des Application Gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c1f09-158">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="c1f09-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1f09-159">CommonParameters</span></span>
<span data-ttu-id="c1f09-160">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1f09-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1f09-161">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1f09-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1f09-162">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c1f09-162">INPUTS</span></span>

### <span data-ttu-id="c1f09-163">Keine</span><span class="sxs-lookup"><span data-stu-id="c1f09-163">None</span></span>

## <span data-ttu-id="c1f09-164">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c1f09-164">OUTPUTS</span></span>

### <span data-ttu-id="c1f09-165">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayPathRule</span><span class="sxs-lookup"><span data-stu-id="c1f09-165">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule</span></span>

## <span data-ttu-id="c1f09-166">Notizen</span><span class="sxs-lookup"><span data-stu-id="c1f09-166">NOTES</span></span>

## <span data-ttu-id="c1f09-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c1f09-167">RELATED LINKS</span></span>

[<span data-ttu-id="c1f09-168">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c1f09-168">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="c1f09-169">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c1f09-169">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="c1f09-170">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c1f09-170">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="c1f09-171">Neu – AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c1f09-171">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="c1f09-172">Neu – AzApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c1f09-172">New-AzApplicationGatewayBackendHttpSettings</span></span>](./New-AzApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="c1f09-173">Neu – AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c1f09-173">New-AzApplicationGatewayPathRuleConfig</span></span>](./New-AzApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="c1f09-174">Neu – AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c1f09-174">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="c1f09-175">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c1f09-175">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="c1f09-176">Satz-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c1f09-176">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


