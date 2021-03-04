---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 2bc6a8eed22660d966256afbc9783e4edfc04947
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936176"
---
# <span data-ttu-id="a7808-101">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a7808-101">Add-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="a7808-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7808-102">SYNOPSIS</span></span>
<span data-ttu-id="a7808-103">Fügt einem Back-End-Serverpool ein Array von URL-Pfadzuordnungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="a7808-103">Adds an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="a7808-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a7808-104">SYNTAX</span></span>

### <span data-ttu-id="a7808-105">Back-EndSetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="a7808-105">BackendSetByResource (Default)</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a7808-106">Back-EndSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a7808-106">BackendSetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> -DefaultBackendAddressPoolId <String>
 -DefaultBackendHttpSettingsId <String> [-DefaultRewriteRuleSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7808-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="a7808-107">RedirectSetByResource</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7808-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a7808-108">RedirectSetByResourceId</span></span>
```
Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSetId <String>]
 -DefaultRedirectConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7808-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a7808-109">DESCRIPTION</span></span>
<span data-ttu-id="a7808-110">Das **Cmdlet Add-AzApplicationGatewayUrlPathMapConfig** fügt einem Back-End-Serverpool ein Array von URL-Pfadzuordnungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="a7808-110">The **Add-AzApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="a7808-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a7808-111">EXAMPLES</span></span>

### <span data-ttu-id="a7808-112">Beispiel 1: Hinzufügen einer URL-Pfadzuordnung zu einem Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="a7808-112">Example 1: Add an URL path mapping to an application gateway.</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $pool = Get-AzApplicationGatewayBackendAddressPool -ApplicationGateway $appgw -Name "pool01"
PS C:\> $poolSettings = Get-AzApplicationGatewayBackendHttpSettings -ApplicationGateway $appgw -Name "poolSettings01"
PS C:\> $pathRule = New-AzApplicationGatewayPathRuleConfig -Name "rule01" -Paths "/path" -BackendAddressPool $pool -BackendHttpSettings $poolSettings
PS C:\> $appgw = Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "url01" -PathRules $pathRule -DefaultBackendAddressPool $pool -DefaultBackendHttpSettings $poolSettings
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="a7808-113">Der erste Befehl ruft ein Anwendungsgateway mit dem Namen "appGwName" ab und speichert es in $appgw Variablen.</span><span class="sxs-lookup"><span data-stu-id="a7808-113">The first command gets an application gateway named appGwName and stores it in $appgw variable.</span></span>
<span data-ttu-id="a7808-114">Der zweite Befehl ruft den Back-End-Adresspool ab und speichert ihn in $pool Variablen.</span><span class="sxs-lookup"><span data-stu-id="a7808-114">The second command gets backend address pool and stores it in $pool variable.</span></span>
<span data-ttu-id="a7808-115">Der dritte Befehl ruft die Back-End-Http-Einstellungen ab und speichert sie in $poolSettings Variable.</span><span class="sxs-lookup"><span data-stu-id="a7808-115">The third command gets backend http settings and stores it in $poolSettings variable.</span></span>
<span data-ttu-id="a7808-116">Mit dem vierten Befehl wird eine neue Pfadregelkonfiguration namens "Regel01" erstellt und in der $pathRule gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a7808-116">The fourth command create new path rule configuration named rule01 and stores it in $pathRule variable.</span></span>
<span data-ttu-id="a7808-117">Der fünfte Befehl fügt dem Anwendungsgateway die Urlpfadzuordnungskonfiguration url01 hinzu.</span><span class="sxs-lookup"><span data-stu-id="a7808-117">The fifth command adds url path mapping configuration named url01 to the application gateway.</span></span>
<span data-ttu-id="a7808-118">Mit dem sechsten Befehl wird das Anwendungsgateway aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a7808-118">The sixth command updates the application gateway.</span></span>

## <span data-ttu-id="a7808-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a7808-119">PARAMETERS</span></span>

### <span data-ttu-id="a7808-120">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a7808-120">-ApplicationGateway</span></span>
<span data-ttu-id="a7808-121">Gibt das Anwendungsgateway an, dem dieses Cmdlet eine URL-Pfadzuordnungskonfiguration hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="a7808-121">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="a7808-122">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a7808-122">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="a7808-123">Gibt den standardmäßigen Back-End-Adresspool an, der weitergeleitet werden soll, falls keine der im *Parameter pathRules* angegebenen Regeln übereinstimmen sollte.</span><span class="sxs-lookup"><span data-stu-id="a7808-123">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: BackendSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7808-124">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="a7808-124">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="a7808-125">Gibt die standardmäßige Back-End-Adresspool-ID an.</span><span class="sxs-lookup"><span data-stu-id="a7808-125">Specifies the default backend address pool ID.</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7808-126">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="a7808-126">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="a7808-127">Gibt die standardmäßigen Back-End-HTTP-Einstellungen an, die für den Fall verwendet werden sollen, dass keine der im *Parameter pathRules* angegebenen Regeln übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a7808-127">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: BackendSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7808-128">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="a7808-128">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="a7808-129">Gibt die standardmäßige HTTP-Einstellungs-ID für das Back-End an.</span><span class="sxs-lookup"><span data-stu-id="a7808-129">Specifies the default backend HTTP settings ID.</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7808-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7808-130">-DefaultProfile</span></span>
<span data-ttu-id="a7808-131">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a7808-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7808-132">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="a7808-132">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="a7808-133">Standardmäßige RedirectConfiguration für Das Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="a7808-133">Application gateway default RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: RedirectSetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7808-134">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="a7808-134">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="a7808-135">ID des Standardmäßigen RedirectConfiguration-Anwendungsgateways</span><span class="sxs-lookup"><span data-stu-id="a7808-135">ID of the application gateway default RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: RedirectSetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7808-136">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a7808-136">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="a7808-137">Standardregelsatz für das Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="a7808-137">Application gateway default rewrite rule set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: BackendSetByResource, RedirectSetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7808-138">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="a7808-138">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="a7808-139">ID des Standardmäßigen Neuschreibregelsatzs für das Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="a7808-139">ID of the application gateway default rewrite rule set</span></span>

```yaml
Type: System.String
Parameter Sets: BackendSetByResourceId, RedirectSetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7808-140">-Name</span><span class="sxs-lookup"><span data-stu-id="a7808-140">-Name</span></span>
<span data-ttu-id="a7808-141">Gibt den Namen der URL-Pfadzuordnung an, den dieses Cmdlet dem Back-End-Serverpool hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="a7808-141">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="a7808-142">-PathRules</span><span class="sxs-lookup"><span data-stu-id="a7808-142">-PathRules</span></span>
<span data-ttu-id="a7808-143">Gibt eine Liste mit Pfadregeln an.</span><span class="sxs-lookup"><span data-stu-id="a7808-143">Specifies a list of path rules.</span></span>
<span data-ttu-id="a7808-144">Die Pfadregeln sind für die Reihenfolge vertraulich, sie werden in der Reihenfolge angewendet, in der sie angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a7808-144">The path rules are order sensitive, they are applied in order they are specified.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7808-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7808-145">CommonParameters</span></span>
<span data-ttu-id="a7808-146">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7808-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7808-147">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7808-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7808-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a7808-148">INPUTS</span></span>

### <span data-ttu-id="a7808-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a7808-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a7808-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a7808-150">OUTPUTS</span></span>

### <span data-ttu-id="a7808-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a7808-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a7808-152">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a7808-152">NOTES</span></span>

## <span data-ttu-id="a7808-153">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a7808-153">RELATED LINKS</span></span>

[<span data-ttu-id="a7808-154">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a7808-154">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="a7808-155">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a7808-155">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="a7808-156">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a7808-156">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="a7808-157">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a7808-157">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


