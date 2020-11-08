---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BBA600C2-4813-4C12-8447-E770A949DA32
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: b0335fd0700b256650809c4548efe4d1e620442b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009162"
---
# <span data-ttu-id="c4fb9-101">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c4fb9-101">Add-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="c4fb9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c4fb9-102">SYNOPSIS</span></span>
<span data-ttu-id="c4fb9-103">Fügt eine Anforderungs Routingregel zu einem Anwendungsgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="c4fb9-103">Adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="c4fb9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4fb9-104">SYNTAX</span></span>

### <span data-ttu-id="c4fb9-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c4fb9-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4fb9-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c4fb9-106">SetByResource</span></span>
```
Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4fb9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4fb9-107">DESCRIPTION</span></span>
<span data-ttu-id="c4fb9-108">Mit dem Cmdlet **Add-AzApplicationGatewayRequestRoutingRule** wird eine Anforderungs Routingregel zu einem Anwendungsgateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c4fb9-108">The **Add-AzApplicationGatewayRequestRoutingRule** cmdlet adds a request routing rule to an application gateway.</span></span>

## <span data-ttu-id="c4fb9-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c4fb9-109">EXAMPLES</span></span>

### <span data-ttu-id="c4fb9-110">Beispiel 1: Hinzufügen einer Anforderungs Routingregel zu einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="c4fb9-110">Example 1: Add a request routing rule to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="c4fb9-111">Der erste Befehl ruft das Anwendungsgateway ab und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="c4fb9-111">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c4fb9-112">Mit dem zweiten Befehl wird die Anforderungs Routingregel dem Anwendungsgateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c4fb9-112">The second command adds the request routing rule to the application gateway.</span></span>

## <span data-ttu-id="c4fb9-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4fb9-113">PARAMETERS</span></span>

### <span data-ttu-id="c4fb9-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c4fb9-114">-ApplicationGateway</span></span>
<span data-ttu-id="c4fb9-115">Gibt ein Anwendungsgateway an, dem dieses Cmdlet eine Anforderungs Routingregel hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="c4fb9-115">Specifies an application gateway to which this cmdlet adds a request routing rule.</span></span>

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

### <span data-ttu-id="c4fb9-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c4fb9-116">-BackendAddressPool</span></span>
<span data-ttu-id="c4fb9-117">Gibt ein Back-End-Adresspool Objekt des Anwendungs Gateways an.</span><span class="sxs-lookup"><span data-stu-id="c4fb9-117">Specifies an application gateway back-end address pool object.</span></span>

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

### <span data-ttu-id="c4fb9-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="c4fb9-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="c4fb9-119">Gibt eine ID des Back-End-Adresspools des Anwendungs Gateways an.</span><span class="sxs-lookup"><span data-stu-id="c4fb9-119">Specifies an application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="c4fb9-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c4fb9-120">-BackendHttpSettings</span></span>
<span data-ttu-id="c4fb9-121">Gibt ein Back-End-HTTP-Einstellungsobjekt für ein Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="c4fb9-121">Specifies a back-end HTTP settings object for an application gateway.</span></span>

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

### <span data-ttu-id="c4fb9-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="c4fb9-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="c4fb9-123">Gibt eine HTTP-Back-End-Einstellungen-ID für ein Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="c4fb9-123">Specifies a backend HTTP settings ID for an application gateway.</span></span>

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

### <span data-ttu-id="c4fb9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4fb9-124">-DefaultProfile</span></span>
<span data-ttu-id="c4fb9-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c4fb9-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4fb9-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="c4fb9-126">-HttpListener</span></span>
<span data-ttu-id="c4fb9-127">Gibt das Application Gateway http-Listener-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="c4fb9-127">Specifies application gateway HTTP listener object.</span></span>

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

### <span data-ttu-id="c4fb9-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="c4fb9-128">-HttpListenerId</span></span>
<span data-ttu-id="c4fb9-129">Gibt die HTTP-Listener-ID des Anwendungs Gateways an.</span><span class="sxs-lookup"><span data-stu-id="c4fb9-129">Specifies application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="c4fb9-130">-Name</span><span class="sxs-lookup"><span data-stu-id="c4fb9-130">-Name</span></span>
<span data-ttu-id="c4fb9-131">Gibt den Namen der Anforderungs Routingregel an, die von diesem Cmdlet hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="c4fb9-131">Specifies the name of request routing rule this cmdlet adds.</span></span>

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

### <span data-ttu-id="c4fb9-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4fb9-132">-RedirectConfiguration</span></span>
<span data-ttu-id="c4fb9-133">Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4fb9-133">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="c4fb9-134">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c4fb9-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="c4fb9-135">ID des Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4fb9-135">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="c4fb9-136">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c4fb9-136">-RewriteRuleSet</span></span>
<span data-ttu-id="c4fb9-137">Application Gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c4fb9-137">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="c4fb9-138">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="c4fb9-138">-RewriteRuleSetId</span></span>
<span data-ttu-id="c4fb9-139">ID des Application Gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="c4fb9-139">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="c4fb9-140">-RuleType</span><span class="sxs-lookup"><span data-stu-id="c4fb9-140">-RuleType</span></span>
<span data-ttu-id="c4fb9-141">Gibt den Typ der Anforderungs Routingregel an.</span><span class="sxs-lookup"><span data-stu-id="c4fb9-141">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="c4fb9-142">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="c4fb9-142">-UrlPathMap</span></span>
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

### <span data-ttu-id="c4fb9-143">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="c4fb9-143">-UrlPathMapId</span></span>
<span data-ttu-id="c4fb9-144">Gibt die URL-Pfad Zuordnungs-ID für die Routingregel an.</span><span class="sxs-lookup"><span data-stu-id="c4fb9-144">Specifies the URL path map ID for the routing rule.</span></span>

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

### <span data-ttu-id="c4fb9-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4fb9-145">CommonParameters</span></span>
<span data-ttu-id="c4fb9-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4fb9-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4fb9-147">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4fb9-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4fb9-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c4fb9-148">INPUTS</span></span>

### <span data-ttu-id="c4fb9-149">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c4fb9-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c4fb9-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c4fb9-150">OUTPUTS</span></span>

### <span data-ttu-id="c4fb9-151">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c4fb9-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c4fb9-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="c4fb9-152">NOTES</span></span>

## <span data-ttu-id="c4fb9-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c4fb9-153">RELATED LINKS</span></span>

[<span data-ttu-id="c4fb9-154">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c4fb9-154">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="c4fb9-155">Neu – AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c4fb9-155">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="c4fb9-156">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c4fb9-156">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="c4fb9-157">Satz-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="c4fb9-157">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


