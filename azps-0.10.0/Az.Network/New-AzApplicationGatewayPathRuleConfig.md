---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: b6722412717d0ef087c2540ff49d3d7a5b87913c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841408"
---
# <span data-ttu-id="47517-101">New-AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="47517-101">New-AzApplicationGatewayPathRuleConfig</span></span>

## <span data-ttu-id="47517-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="47517-102">SYNOPSIS</span></span>
<span data-ttu-id="47517-103">Erstellt eine Anwendungsgateway-Pfadregel.</span><span class="sxs-lookup"><span data-stu-id="47517-103">Creates an application gateway path rule.</span></span>

## <span data-ttu-id="47517-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="47517-104">SYNTAX</span></span>

### <span data-ttu-id="47517-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="47517-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47517-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="47517-106">SetByResource</span></span>
```
New-AzApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47517-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47517-107">DESCRIPTION</span></span>
<span data-ttu-id="47517-108">Das Cmdlet **New-AzApplicationGatewayPathRuleConfig** erstellt eine Pfadregel für das Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="47517-108">The **New-AzApplicationGatewayPathRuleConfig** cmdlet creates an application gateway path rule.</span></span>
<span data-ttu-id="47517-109">Von diesem Cmdlet erstellte Regeln können einer Sammlung von URL-Pfad Zuordnungs Konfigurationseinstellungen hinzugefügt und dann einem Gateway zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="47517-109">Rules created by this cmdlet can be added to a collection of URL path map configuration settings and then assigned to a gateway.</span></span>

<span data-ttu-id="47517-110">Konfigurationseinstellungen für Pfad Zuordnungen werden im Lastenausgleich des Anwendungs Gateways verwendet.</span><span class="sxs-lookup"><span data-stu-id="47517-110">Path map configuration settings are used in application gateway load balancing.</span></span>

## <span data-ttu-id="47517-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="47517-111">EXAMPLES</span></span>

### <span data-ttu-id="47517-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="47517-112">Example 1</span></span>
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSetting -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

<span data-ttu-id="47517-113">Mit diesen Befehlen wird eine neue Anwendungsgateway-Pfadregel erstellt, und dann wird das Cmdlet **Add-AzApplicationGatewayUrlPathMapConfig** verwendet, um die Regel einem Anwendungsgateway zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="47517-113">These commands create a new application gateway path rule and then use the **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet to assign that rule to an application gateway.</span></span>
<span data-ttu-id="47517-114">Dazu erstellt der erste Befehl einen Objektverweis auf das Gateway-ContosoApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="47517-114">To do this, the first command creates an object reference to the gateway ContosoApplicationGateway.</span></span>
<span data-ttu-id="47517-115">Dieser Objektverweis wird in einer Variablen mit dem Namen $Gateway gespeichert.</span><span class="sxs-lookup"><span data-stu-id="47517-115">This object reference is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="47517-116">Mit den nächsten beiden Befehlen wird ein Back-End-Adresspool und ein Back-End-HTTP-Einstellungsobjekt erstellt. Diese Objekte (in den Variablen $AddressPool und $HttpSettings gespeichert) werden benötigt, um ein Pfadregel-Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="47517-116">The next two commands create a backend address pool and a backend HTTP settings object; these objects (stored in the variables $AddressPool and $HttpSettings) are needed in order to create a path rule object.</span></span>

<span data-ttu-id="47517-117">Der vierte Befehl erstellt das Pfadregel-Objekt und wird in einer Variablen mit dem Namen $PathRuleConfig gespeichert.</span><span class="sxs-lookup"><span data-stu-id="47517-117">The fourth command creates the path rule object and is stored in a variable named $PathRuleConfig.</span></span>

<span data-ttu-id="47517-118">Der fünfte Befehl verwendet **Add-AzApplicationGatewayUrlPathMapConfig** , um die Konfigurationseinstellungen und die neue Pfadregel, die in diesen Einstellungen enthalten ist, ContosoApplicationGateway hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="47517-118">The fifth command uses **Add-AzApplicationGatewayUrlPathMapConfig** to add the configuration settings and the new path rule contained within those settings to ContosoApplicationGateway.</span></span>

## <span data-ttu-id="47517-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="47517-119">PARAMETERS</span></span>

### <span data-ttu-id="47517-120">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="47517-120">-BackendAddressPool</span></span>
<span data-ttu-id="47517-121">Gibt einen Objektverweis auf eine Sammlung von Einstellungen des Back-End-Adresspools an, die den Konfigurationseinstellungen für Gateway-Pfadregeln hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="47517-121">Specifies an object reference to a collection of backend address pool settings to be added to the gateway path rules configuration settings.</span></span>
<span data-ttu-id="47517-122">Sie können diesen Objektverweis mithilfe des New-AzApplicationGatewayBackendAddressPool-Cmdlets und der Syntax wie folgt erstellen:</span><span class="sxs-lookup"><span data-stu-id="47517-122">You can create this object reference by using the New-AzApplicationGatewayBackendAddressPool cmdlet and syntax similar to this:</span></span>

`$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`

<span data-ttu-id="47517-123">Der vorhergehende Befehl fügt dem Adresspool zwei IP-Adressen (192.16.1.1 und 192.168.1.2) hinzu.</span><span class="sxs-lookup"><span data-stu-id="47517-123">The preceding command adds two IP addresses (192.16.1.1 and 192.168.1.2) to the address pool.</span></span>
<span data-ttu-id="47517-124">Beachten Sie, dass die IP-Adresse in Anführungszeichen eingeschlossen und durch Kommas getrennt wird.</span><span class="sxs-lookup"><span data-stu-id="47517-124">Note that the IP address are enclosed in quote marks and separated by using commas.</span></span>

<span data-ttu-id="47517-125">Die resultierende Variable $AddressPool kann dann als Parameterwert für den *DefaultBackendAddressPool* -Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="47517-125">The resulting variable, $AddressPool, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter.</span></span>

<span data-ttu-id="47517-126">Der Back-End-Adresspool stellt die IP-Adressen auf den Back-End-Servern dar.</span><span class="sxs-lookup"><span data-stu-id="47517-126">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="47517-127">Diese IP-Adressen sollten entweder zum Subnetz des virtuellen Netzwerks gehören oder öffentliche IP-Adressen sein.</span><span class="sxs-lookup"><span data-stu-id="47517-127">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>
<span data-ttu-id="47517-128">Wenn Sie diesen Parameter verwenden, können Sie den *DefaultBackendAddressPoolId* -Parameter nicht im gleichen Befehl verwenden.</span><span class="sxs-lookup"><span data-stu-id="47517-128">If you use this parameter you cannot use the *DefaultBackendAddressPoolId* parameter in the same command.</span></span>

```yaml
Type: PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47517-129">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="47517-129">-BackendAddressPoolId</span></span>
<span data-ttu-id="47517-130">Gibt die ID eines vorhandenen Back-End-Adresspools an, der den Konfigurationseinstellungen für Gateway-Pfad Regel hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="47517-130">Specifies the ID of an existing backend address pool that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="47517-131">Adresspool-IDs können mithilfe des Get-AzApplicationGatewayBackendAddressPool-Cmdlets zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="47517-131">Address pool IDs can be returned by using the Get-AzApplicationGatewayBackendAddressPool cmdlet.</span></span>
<span data-ttu-id="47517-132">Nachdem Sie die ID haben, können Sie den *DefaultBackendAddressPoolId* -Parameter anstelle des *DefaultBackendAddressPool* -Parameters verwenden.</span><span class="sxs-lookup"><span data-stu-id="47517-132">After you have the ID you can then use the *DefaultBackendAddressPoolId* parameter instead of the *DefaultBackendAddressPool* parameter.</span></span>
<span data-ttu-id="47517-133">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="47517-133">For instance:</span></span>

<span data-ttu-id="47517-134">-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool"</span><span class="sxs-lookup"><span data-stu-id="47517-134">-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool"</span></span>

<span data-ttu-id="47517-135">Der Back-End-Adresspool stellt die IP-Adressen auf den Back-End-Servern dar.</span><span class="sxs-lookup"><span data-stu-id="47517-135">The backend address pool represents the IP addresses on the backend servers.</span></span>
<span data-ttu-id="47517-136">Diese IP-Adressen sollten entweder zum Subnetz des virtuellen Netzwerks gehören oder öffentliche IP-Adressen sein.</span><span class="sxs-lookup"><span data-stu-id="47517-136">These IP addresses should either belong to the virtual network subnet or should be public IP addresses.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47517-137">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="47517-137">-BackendHttpSettings</span></span>
<span data-ttu-id="47517-138">Gibt einen Objektverweis auf eine Sammlung von Back-End-HTTP-Einstellungen an, die den Konfigurationseinstellungen für Gateway-Pfad Regel hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="47517-138">Specifies an object reference to a collection of backend HTTP settings to be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="47517-139">Sie können diesen Objektverweis mithilfe des New-AzApplicationGatewayBackendHttpSetting-Cmdlets und der Syntax wie folgt erstellen:</span><span class="sxs-lookup"><span data-stu-id="47517-139">You can create this object reference by using the New-AzApplicationGatewayBackendHttpSetting cmdlet and syntax similar to this:</span></span>

<span data-ttu-id="47517-140">$HttpSettings = New-AzApplicationGatewayBackendHttpSetting-Name "ContosoHttpSetings"-Port 80-Protokoll "http"-CookieBasedAffinity "deaktiviert"</span><span class="sxs-lookup"><span data-stu-id="47517-140">$HttpSettings = New-AzApplicationGatewayBackendHttpSetting -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"</span></span>

<span data-ttu-id="47517-141">Die resultierende Variable $HttpSettings kann dann als Parameterwert für den *DefaultBackendAddressPool* -Parameter verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="47517-141">The resulting variable, $HttpSettings, can then be used as the parameter value for the *DefaultBackendAddressPool* parameter:</span></span>

<span data-ttu-id="47517-142">-DefaultBackendHttpSettings $HttpSettings</span><span class="sxs-lookup"><span data-stu-id="47517-142">-DefaultBackendHttpSettings $HttpSettings</span></span>

<span data-ttu-id="47517-143">Die HTTP-Back-End-Einstellungen konfigurieren Eigenschaften wie Port-, Protokoll-und Cookie-basierter Affinität für einen Back-End-Pool.</span><span class="sxs-lookup"><span data-stu-id="47517-143">The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="47517-144">Wenn Sie diesen Parameter verwenden, können Sie den *DefaultBackendHttpSettingsId* -Parameter nicht im gleichen Befehl verwenden.</span><span class="sxs-lookup"><span data-stu-id="47517-144">If you use this parameter you cannot use the *DefaultBackendHttpSettingsId* parameter in the same command.</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47517-145">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="47517-145">-BackendHttpSettingsId</span></span>
<span data-ttu-id="47517-146">Gibt die ID einer vorhandenen Back-End-HTTP-Einstellungs Sammlung an, die den Konfigurationseinstellungen für Gateway-Pfad Regel hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="47517-146">Specifies the ID of an existing backend HTTP settings collection that can be added to the gateway path rule configuration settings.</span></span>
<span data-ttu-id="47517-147">HTTP-Einstellungs-IDs können mithilfe des Get-AzApplicationGatewayBackendHttpSetting-Cmdlets zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="47517-147">HTTP setting IDs can be returned by using the Get-AzApplicationGatewayBackendHttpSetting cmdlet.</span></span>
<span data-ttu-id="47517-148">Nachdem Sie die ID haben, können Sie den *DefaultBackendHttpSettingsId* -Parameter anstelle des *DefaultBackendHttpSettings* -Parameters verwenden.</span><span class="sxs-lookup"><span data-stu-id="47517-148">After you have the ID you can then use the *DefaultBackendHttpSettingsId* parameter instead of the *DefaultBackendHttpSettings* parameter.</span></span>
<span data-ttu-id="47517-149">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="47517-149">For instance:</span></span>

<span data-ttu-id="47517-150">-DefaultBackendSettings-ID "/Subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-RG/Providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings"</span><span class="sxs-lookup"><span data-stu-id="47517-150">-DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings"</span></span>

<span data-ttu-id="47517-151">Die HTTP-Back-End-Einstellungen konfigurieren Eigenschaften wie Port-, Protokoll-und Cookie-basierter Affinität für einen Back-End-Pool.</span><span class="sxs-lookup"><span data-stu-id="47517-151">The backend HTTP settings configure properties such as port, protocol, and cookie-based affinity for a backend pool.</span></span>
<span data-ttu-id="47517-152">Wenn Sie diesen Parameter verwenden, können Sie den *DefaultBackendHttpSettings* -Parameter nicht im gleichen Befehl verwenden.</span><span class="sxs-lookup"><span data-stu-id="47517-152">If you use this parameter you cannot use the *DefaultBackendHttpSettings* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47517-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47517-153">-DefaultProfile</span></span>
<span data-ttu-id="47517-154">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="47517-154">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47517-155">-Name</span><span class="sxs-lookup"><span data-stu-id="47517-155">-Name</span></span>
<span data-ttu-id="47517-156">Gibt den Namen der vom Cmdlet erstellten Pfad Regelkonfiguration an.</span><span class="sxs-lookup"><span data-stu-id="47517-156">Specifies the name of the path rule configuration that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47517-157">-Pfade</span><span class="sxs-lookup"><span data-stu-id="47517-157">-Paths</span></span>
<span data-ttu-id="47517-158">Gibt mindestens eine Application Gateway Path-Regel an.</span><span class="sxs-lookup"><span data-stu-id="47517-158">Specifies one or more application gateway path rules.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47517-159">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="47517-159">-RedirectConfiguration</span></span>
<span data-ttu-id="47517-160">Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="47517-160">Application gateway RedirectConfiguration</span></span>

```yaml
Type: PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47517-161">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="47517-161">-RedirectConfigurationId</span></span>
<span data-ttu-id="47517-162">ID des Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="47517-162">ID of the application gateway RedirectConfiguration</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47517-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47517-163">CommonParameters</span></span>
<span data-ttu-id="47517-164">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47517-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47517-165">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47517-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47517-166">Eingaben</span><span class="sxs-lookup"><span data-stu-id="47517-166">INPUTS</span></span>

###  
<span data-ttu-id="47517-167">**New-AzApplicationGatewayPathRuleConfig** akzeptiert keine Pipeline-Eingabe.</span><span class="sxs-lookup"><span data-stu-id="47517-167">**New-AzApplicationGatewayPathRuleConfig** does not accept pipelined input.</span></span>

## <span data-ttu-id="47517-168">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="47517-168">OUTPUTS</span></span>

###  
<span data-ttu-id="47517-169">**New-AzApplicationGatewayPathRuleConfig** erstellt neue Instanzen des **Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayPathRule** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="47517-169">**New-AzApplicationGatewayPathRuleConfig** creates new instances of the **Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule** object.</span></span>

## <span data-ttu-id="47517-170">Notizen</span><span class="sxs-lookup"><span data-stu-id="47517-170">NOTES</span></span>

## <span data-ttu-id="47517-171">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="47517-171">RELATED LINKS</span></span>

[<span data-ttu-id="47517-172">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="47517-172">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="47517-173">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="47517-173">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="47517-174">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="47517-174">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="47517-175">Neu – AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="47517-175">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="47517-176">Neu – AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="47517-176">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="47517-177">Neu – AzApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="47517-177">New-AzApplicationGatewayPathRuleConfig</span></span>](./New-AzApplicationGatewayPathRuleConfig.md)

[<span data-ttu-id="47517-178">Neu – AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="47517-178">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="47517-179">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="47517-179">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="47517-180">Satz-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="47517-180">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


