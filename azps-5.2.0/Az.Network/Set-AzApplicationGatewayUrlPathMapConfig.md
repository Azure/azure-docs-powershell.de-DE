---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: ec2eede30b6aef81210582b95b775200c8145943
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371312"
---
# <span data-ttu-id="c1487-101">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c1487-101">Set-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="c1487-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1487-102">SYNOPSIS</span></span>
<span data-ttu-id="c1487-103">Legt die Konfiguration für ein Array von URL-Pfadzuordnungen zu einem Back-End-Server-Pool fest.</span><span class="sxs-lookup"><span data-stu-id="c1487-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="c1487-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c1487-104">SYNTAX</span></span>

### <span data-ttu-id="c1487-105">Back-EndByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="c1487-105">BackendSetByResource (Default)</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]>
 -DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>
 -DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c1487-106">Back-EndByResourceId</span><span class="sxs-lookup"><span data-stu-id="c1487-106">BackendSetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> -DefaultBackendAddressPoolId <String>
 -DefaultBackendHttpSettingsId <String> [-DefaultRewriteRuleSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1487-107">RedirectSetByResource</span><span class="sxs-lookup"><span data-stu-id="c1487-107">RedirectSetByResource</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 -DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1487-108">RedirectSetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c1487-108">RedirectSetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <PSApplicationGatewayPathRule[]> [-DefaultRewriteRuleSetId <String>]
 -DefaultRedirectConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1487-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c1487-109">DESCRIPTION</span></span>
<span data-ttu-id="c1487-110">Das **Cmdlet Set-AzApplicationGatewayUrlPathMapConfig** legt die Konfiguration für ein Array von URL-Pfadzuordnungen zu einem Back-End-Serverpool fest.</span><span class="sxs-lookup"><span data-stu-id="c1487-110">The **Set-AzApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="c1487-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c1487-111">EXAMPLES</span></span>

### <span data-ttu-id="c1487-112">Beispiel 1: Aktualisieren einer URL-Pfadzuordnung</span><span class="sxs-lookup"><span data-stu-id="c1487-112">Example 1: Update an URL path mapping</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "map01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="c1487-113">Der erste Befehl ruft das Anwendungsgateway namens "appGwName" ab und speichert das Ergebnis in der $appgw Variable.</span><span class="sxs-lookup"><span data-stu-id="c1487-113">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="c1487-114">Mit dem zweiten Befehl wird die URL-Pfadzuordnung namens "map01" im Anwendungsgateway aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="c1487-114">The second command updates the URL path mapping named map01 in the application gateway.</span></span>
<span data-ttu-id="c1487-115">Mit dem dritten Befehl wird das Anwendungsgateway aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="c1487-115">The third command updates the application gateway.</span></span>

## <span data-ttu-id="c1487-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1487-116">PARAMETERS</span></span>

### <span data-ttu-id="c1487-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c1487-117">-ApplicationGateway</span></span>
<span data-ttu-id="c1487-118">Gibt das Anwendungsgateway an, zu dem dieses Cmdlet eine Konfiguration der URL-Pfadzuordnung legt.</span><span class="sxs-lookup"><span data-stu-id="c1487-118">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

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

### <span data-ttu-id="c1487-119">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c1487-119">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="c1487-120">Gibt den standardmäßigen Back-End-Adresspool an, der weitergeleitet werden soll, falls keine der im Parameter *"pathRules" angegebenen Regeln* zustimmt.</span><span class="sxs-lookup"><span data-stu-id="c1487-120">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="c1487-121">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="c1487-121">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="c1487-122">Gibt die standardmäßige Back-End-Adresspool-ID an.</span><span class="sxs-lookup"><span data-stu-id="c1487-122">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="c1487-123">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c1487-123">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="c1487-124">Gibt die standardmäßigen BACK-End-HTTP-Einstellungen an, die für den Fall verwendet werden sollen, dass keine der im Parameter *"pathRules" angegebenen Regeln* zustimmt.</span><span class="sxs-lookup"><span data-stu-id="c1487-124">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="c1487-125">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="c1487-125">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="c1487-126">Gibt die standardmäßige HTTP-Einstellungs-ID des Backends an.</span><span class="sxs-lookup"><span data-stu-id="c1487-126">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="c1487-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1487-127">-DefaultProfile</span></span>
<span data-ttu-id="c1487-128">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c1487-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1487-129">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c1487-129">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="c1487-130">Standardmäßige Umleitungskonfiguration des Anwendungsgateways</span><span class="sxs-lookup"><span data-stu-id="c1487-130">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="c1487-131">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c1487-131">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="c1487-132">ID des standardmäßigen Anwendungsgateways "RedirectConfiguration"</span><span class="sxs-lookup"><span data-stu-id="c1487-132">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="c1487-133">-DefaultRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c1487-133">-DefaultRewriteRuleSet</span></span>
<span data-ttu-id="c1487-134">Anwendungsgateway, Standardregelsatz für neu schreiben</span><span class="sxs-lookup"><span data-stu-id="c1487-134">Application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="c1487-135">-DefaultRewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="c1487-135">-DefaultRewriteRuleSetId</span></span>
<span data-ttu-id="c1487-136">ID des Standardmäßigen Regelsets für Neuschreibung des Anwendungsgateways</span><span class="sxs-lookup"><span data-stu-id="c1487-136">ID of the application gateway default rewrite rule set</span></span>

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

### <span data-ttu-id="c1487-137">-Name</span><span class="sxs-lookup"><span data-stu-id="c1487-137">-Name</span></span>
<span data-ttu-id="c1487-138">Gibt den Namen der URL-Pfadzuordnung an, für den dieses Cmdlet die Konfiguration vorgibt.</span><span class="sxs-lookup"><span data-stu-id="c1487-138">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

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

### <span data-ttu-id="c1487-139">-PathRules</span><span class="sxs-lookup"><span data-stu-id="c1487-139">-PathRules</span></span>
<span data-ttu-id="c1487-140">Gibt eine Liste von Pfadregeln an.</span><span class="sxs-lookup"><span data-stu-id="c1487-140">Specifies a list of path rules.</span></span>
<span data-ttu-id="c1487-141">Beachten Sie, dass bei den Pfadregeln die Reihenfolge beachtet wird. Sie werden in der Reihenfolge ihrer Angabe angewendet.</span><span class="sxs-lookup"><span data-stu-id="c1487-141">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="c1487-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1487-142">CommonParameters</span></span>
<span data-ttu-id="c1487-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1487-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1487-144">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1487-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1487-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c1487-145">INPUTS</span></span>

### <span data-ttu-id="c1487-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c1487-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c1487-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c1487-147">OUTPUTS</span></span>

### <span data-ttu-id="c1487-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c1487-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c1487-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c1487-149">NOTES</span></span>

## <span data-ttu-id="c1487-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c1487-150">RELATED LINKS</span></span>

[<span data-ttu-id="c1487-151">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c1487-151">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="c1487-152">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c1487-152">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="c1487-153">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c1487-153">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="c1487-154">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="c1487-154">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)


