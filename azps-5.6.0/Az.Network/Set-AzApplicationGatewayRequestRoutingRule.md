---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75A4826A-7A5F-4742-9DC4-DC728CED63D0
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 832fd96f34e18413bfd72e1a05826954f3ae58e4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945796"
---
# <span data-ttu-id="5c7c7-101">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="5c7c7-101">Set-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="5c7c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c7c7-102">SYNOPSIS</span></span>
<span data-ttu-id="5c7c7-103">Ändert eine Anforderungsroutingregel für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="5c7c7-103">Modifies a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="5c7c7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5c7c7-104">SYNTAX</span></span>

### <span data-ttu-id="5c7c7-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5c7c7-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c7c7-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="5c7c7-106">SetByResource</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-Priority <Int32>] [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c7c7-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5c7c7-107">DESCRIPTION</span></span>
<span data-ttu-id="5c7c7-108">Das **Cmdlet Set-AzApplicationGatewayRequestRoutingRule** ändert eine Anforderungsroutingregel.</span><span class="sxs-lookup"><span data-stu-id="5c7c7-108">The **Set-AzApplicationGatewayRequestRoutingRule** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="5c7c7-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5c7c7-109">EXAMPLES</span></span>

### <span data-ttu-id="5c7c7-110">Beispiel 1: Aktualisieren einer Anforderungsroutingregel</span><span class="sxs-lookup"><span data-stu-id="5c7c7-110">Example 1: Update a request routing rule</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -Priority 100 -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="5c7c7-111">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="5c7c7-111">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="5c7c7-112">Der zweite Befehl ändert die Anforderungsroutingregel für das Anwendungsgateway, um die in der Variablen $Setting angegebenen Back-End-HTTP-Einstellungen, einen in der Variablen $Listener angegebenen HTTP-Listener und einen Back-End-Adresspool zu verwenden, der in der $Pool-Variable angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="5c7c7-112">The second command modifies the request routing rule for the application gateway to use back-end HTTP settings specified in the $Setting variable, an HTTP listener specified in the $Listener variable, and a back-end address pool specified in the $Pool variable.</span></span>

## <span data-ttu-id="5c7c7-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5c7c7-113">PARAMETERS</span></span>

### <span data-ttu-id="5c7c7-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5c7c7-114">-ApplicationGateway</span></span>
<span data-ttu-id="5c7c7-115">Gibt das Anwendungsgatewayobjekt an, dem dieses Cmdlet eine Anforderungsroutingregel zurät.</span><span class="sxs-lookup"><span data-stu-id="5c7c7-115">Specifies the application gateway object with which this cmdlet associates a request routing rule.</span></span>

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

### <span data-ttu-id="5c7c7-116">-Back-EndAddressPool</span><span class="sxs-lookup"><span data-stu-id="5c7c7-116">-BackendAddressPool</span></span>
<span data-ttu-id="5c7c7-117">Gibt den Back-End-Adresspool des Anwendungsgateways an.</span><span class="sxs-lookup"><span data-stu-id="5c7c7-117">Specifies the application gateway back-end address pool.</span></span>

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

### <span data-ttu-id="5c7c7-118">-Back-EndAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="5c7c7-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="5c7c7-119">Gibt die Back-End-Adresspool-ID des Anwendungsgateways an.</span><span class="sxs-lookup"><span data-stu-id="5c7c7-119">Specifies the application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="5c7c7-120">-Back-EndHttpSettings</span><span class="sxs-lookup"><span data-stu-id="5c7c7-120">-BackendHttpSettings</span></span>
<span data-ttu-id="5c7c7-121">Gibt die HTTP-Einstellungen für das Anwendungsgateway-Back-End an.</span><span class="sxs-lookup"><span data-stu-id="5c7c7-121">Specifies the application gateway backend HTTP settings.</span></span>

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

### <span data-ttu-id="5c7c7-122">-Back-EndHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="5c7c7-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="5c7c7-123">Gibt die BACK-End-HTTP-Einstellungs-ID des Anwendungsgateways an.</span><span class="sxs-lookup"><span data-stu-id="5c7c7-123">Specifies the application gateway back-end HTTP settings ID.</span></span>

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

### <span data-ttu-id="5c7c7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c7c7-124">-DefaultProfile</span></span>
<span data-ttu-id="5c7c7-125">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5c7c7-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c7c7-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="5c7c7-126">-HttpListener</span></span>
<span data-ttu-id="5c7c7-127">Gibt den HTTP-Listener für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="5c7c7-127">Specifies the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="5c7c7-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="5c7c7-128">-HttpListenerId</span></span>
<span data-ttu-id="5c7c7-129">Gibt die HTTP-Listener-ID des Anwendungsgateways an.</span><span class="sxs-lookup"><span data-stu-id="5c7c7-129">Specifies the application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="5c7c7-130">-Name</span><span class="sxs-lookup"><span data-stu-id="5c7c7-130">-Name</span></span>
<span data-ttu-id="5c7c7-131">Gibt den Namen der Anforderungsroutingregel an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="5c7c7-131">Specifies the name of the request routing rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="5c7c7-132">-Priorität</span><span class="sxs-lookup"><span data-stu-id="5c7c7-132">-Priority</span></span>
<span data-ttu-id="5c7c7-133">Die Priorität der Regel</span><span class="sxs-lookup"><span data-stu-id="5c7c7-133">The priority of the rule</span></span>

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

### <span data-ttu-id="5c7c7-134">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c7c7-134">-RedirectConfiguration</span></span>
<span data-ttu-id="5c7c7-135">RedirectConfiguration des Anwendungsgateways</span><span class="sxs-lookup"><span data-stu-id="5c7c7-135">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="5c7c7-136">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="5c7c7-136">-RedirectConfigurationId</span></span>
<span data-ttu-id="5c7c7-137">ID des Anwendungsgateways RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c7c7-137">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="5c7c7-138">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5c7c7-138">-RewriteRuleSet</span></span>
<span data-ttu-id="5c7c7-139">Anwendungsgateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5c7c7-139">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="5c7c7-140">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="5c7c7-140">-RewriteRuleSetId</span></span>
<span data-ttu-id="5c7c7-141">ID des Anwendungsgateways RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="5c7c7-141">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="5c7c7-142">-RuleType</span><span class="sxs-lookup"><span data-stu-id="5c7c7-142">-RuleType</span></span>
<span data-ttu-id="5c7c7-143">Gibt den Typ der Anforderungsroutingregel an.</span><span class="sxs-lookup"><span data-stu-id="5c7c7-143">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="5c7c7-144">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="5c7c7-144">-UrlPathMap</span></span>
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

### <span data-ttu-id="5c7c7-145">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="5c7c7-145">-UrlPathMapId</span></span>
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

### <span data-ttu-id="5c7c7-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c7c7-146">CommonParameters</span></span>
<span data-ttu-id="5c7c7-147">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c7c7-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c7c7-148">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c7c7-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c7c7-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5c7c7-149">INPUTS</span></span>

### <span data-ttu-id="5c7c7-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5c7c7-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5c7c7-151">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5c7c7-151">OUTPUTS</span></span>

### <span data-ttu-id="5c7c7-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5c7c7-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5c7c7-153">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5c7c7-153">NOTES</span></span>

## <span data-ttu-id="5c7c7-154">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5c7c7-154">RELATED LINKS</span></span>

[<span data-ttu-id="5c7c7-155">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="5c7c7-155">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="5c7c7-156">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="5c7c7-156">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="5c7c7-157">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="5c7c7-157">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="5c7c7-158">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="5c7c7-158">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)


