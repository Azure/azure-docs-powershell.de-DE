---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BBA600C2-4813-4C12-8447-E770A949DA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 858af0fc06dc9df00eec100c3d07306797e99b56
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469323"
---
# <span data-ttu-id="eb4d9-101">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="eb4d9-101">Add-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="eb4d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb4d9-102">SYNOPSIS</span></span>
<span data-ttu-id="eb4d9-103">Fügt einem Anwendungsgateway eine Anforderungsroutingregel hinzu.</span><span class="sxs-lookup"><span data-stu-id="eb4d9-103">Adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="eb4d9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eb4d9-104">SYNTAX</span></span>

### <span data-ttu-id="eb4d9-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="eb4d9-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb4d9-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="eb4d9-106">SetByResource</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb4d9-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eb4d9-107">DESCRIPTION</span></span>
<span data-ttu-id="eb4d9-108">Das **Cmdlet "Add-AzApplicationGatewayRequestRoutingRule"** fügt einem Anwendungsgateway eine Anforderungsroutingregel hinzu.</span><span class="sxs-lookup"><span data-stu-id="eb4d9-108">The **Add-AzApplicationGatewayRequestRoutingRule** cmdlet adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="eb4d9-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="eb4d9-109">EXAMPLES</span></span>

### <span data-ttu-id="eb4d9-110">Beispiel 1: Hinzufügen einer Anforderungsroutingregel zu einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="eb4d9-110">Example 1: Add a request routing rule to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -Priority 100 -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="eb4d9-111">Der erste Befehl ruft das Anwendungsgateway ab und speichert es in der $AppGw Variable.</span><span class="sxs-lookup"><span data-stu-id="eb4d9-111">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="eb4d9-112">Der zweite Befehl fügt dem Anwendungsgateway die Anforderungsroutingregel hinzu.</span><span class="sxs-lookup"><span data-stu-id="eb4d9-112">The second command adds the request routing rule to the application gateway.</span></span>

## <span data-ttu-id="eb4d9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb4d9-113">PARAMETERS</span></span>

### <span data-ttu-id="eb4d9-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eb4d9-114">-ApplicationGateway</span></span>
<span data-ttu-id="eb4d9-115">Gibt ein Anwendungsgateway an, dem dieses Cmdlet eine Anforderungsroutingregel hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="eb4d9-115">Specifies an application gateway to which this cmdlet adds a request routing rule.</span></span>

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

### <span data-ttu-id="eb4d9-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="eb4d9-116">-BackendAddressPool</span></span>
<span data-ttu-id="eb4d9-117">Gibt ein Back-End-Adresspoolobjekt des Anwendungsgateways an.</span><span class="sxs-lookup"><span data-stu-id="eb4d9-117">Specifies an application gateway back-end address pool object.</span></span>

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

### <span data-ttu-id="eb4d9-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="eb4d9-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="eb4d9-119">Gibt eine Back-End-Adresspool-ID des Anwendungsgateways an.</span><span class="sxs-lookup"><span data-stu-id="eb4d9-119">Specifies an application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="eb4d9-120">-Back-EndHttpSettings</span><span class="sxs-lookup"><span data-stu-id="eb4d9-120">-BackendHttpSettings</span></span>
<span data-ttu-id="eb4d9-121">Gibt ein Back-End-HTTP-Einstellungsobjekt für ein Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="eb4d9-121">Specifies a back-end HTTP settings object for an application gateway.</span></span>

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

### <span data-ttu-id="eb4d9-122">-Back-EndHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="eb4d9-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="eb4d9-123">Gibt eine Back-End-HTTP-Einstellungs-ID für ein Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="eb4d9-123">Specifies a backend HTTP settings ID for an application gateway.</span></span>

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

### <span data-ttu-id="eb4d9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb4d9-124">-DefaultProfile</span></span>
<span data-ttu-id="eb4d9-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eb4d9-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb4d9-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="eb4d9-126">-HttpListener</span></span>
<span data-ttu-id="eb4d9-127">Gibt das HTTP-Listenerobjekt des Anwendungsgateways an.</span><span class="sxs-lookup"><span data-stu-id="eb4d9-127">Specifies application gateway HTTP listener object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb4d9-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="eb4d9-128">-HttpListenerId</span></span>
<span data-ttu-id="eb4d9-129">Gibt die HTTP-Listener-ID des Anwendungsgateways an.</span><span class="sxs-lookup"><span data-stu-id="eb4d9-129">Specifies application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="eb4d9-130">-Name</span><span class="sxs-lookup"><span data-stu-id="eb4d9-130">-Name</span></span>
<span data-ttu-id="eb4d9-131">Gibt den Namen der Anforderungsroutingregel an, die dieses Cmdlet hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="eb4d9-131">Specifies the name of request routing rule this cmdlet adds.</span></span>

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

### <span data-ttu-id="eb4d9-132">-Priority</span><span class="sxs-lookup"><span data-stu-id="eb4d9-132">-Priority</span></span>
<span data-ttu-id="eb4d9-133">Die Priorität der Regel</span><span class="sxs-lookup"><span data-stu-id="eb4d9-133">The priority of the rule</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:
Accepted Values: 1-20000

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb4d9-134">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="eb4d9-134">-RedirectConfiguration</span></span>
<span data-ttu-id="eb4d9-135">Anwendungsgateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="eb4d9-135">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="eb4d9-136">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="eb4d9-136">-RedirectConfigurationId</span></span>
<span data-ttu-id="eb4d9-137">ID des Anwendungsgateways RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="eb4d9-137">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="eb4d9-138">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="eb4d9-138">-RewriteRuleSet</span></span>
<span data-ttu-id="eb4d9-139">Application gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="eb4d9-139">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="eb4d9-140">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="eb4d9-140">-RewriteRuleSetId</span></span>
<span data-ttu-id="eb4d9-141">ID des Anwendungsgateways "RewriteRuleSet"</span><span class="sxs-lookup"><span data-stu-id="eb4d9-141">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="eb4d9-142">-RuleType</span><span class="sxs-lookup"><span data-stu-id="eb4d9-142">-RuleType</span></span>
<span data-ttu-id="eb4d9-143">Gibt den Typ der Anforderungsroutingregel an.</span><span class="sxs-lookup"><span data-stu-id="eb4d9-143">Specifies the type of request routing rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, PathBasedRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb4d9-144">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="eb4d9-144">-UrlPathMap</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb4d9-145">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="eb4d9-145">-UrlPathMapId</span></span>
<span data-ttu-id="eb4d9-146">Gibt die URL-Pfadzuordnungs-ID für die Routingregel an.</span><span class="sxs-lookup"><span data-stu-id="eb4d9-146">Specifies the URL path map ID for the routing rule.</span></span>

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

### <span data-ttu-id="eb4d9-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb4d9-147">CommonParameters</span></span>
<span data-ttu-id="eb4d9-148">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb4d9-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb4d9-149">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eb4d9-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb4d9-150">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="eb4d9-150">INPUTS</span></span>

### <span data-ttu-id="eb4d9-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eb4d9-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="eb4d9-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="eb4d9-152">OUTPUTS</span></span>

### <span data-ttu-id="eb4d9-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="eb4d9-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="eb4d9-154">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="eb4d9-154">NOTES</span></span>

## <span data-ttu-id="eb4d9-155">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="eb4d9-155">RELATED LINKS</span></span>

[<span data-ttu-id="eb4d9-156">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="eb4d9-156">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="eb4d9-157">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="eb4d9-157">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="eb4d9-158">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="eb4d9-158">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="eb4d9-159">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="eb4d9-159">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


