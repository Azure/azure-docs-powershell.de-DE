---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75A4826A-7A5F-4742-9DC4-DC728CED63D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 2e323170bac22950b9a6ca479e8470630741c2bc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174280"
---
# <span data-ttu-id="0ad63-101">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0ad63-101">Set-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="0ad63-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0ad63-102">SYNOPSIS</span></span>
<span data-ttu-id="0ad63-103">Ändert eine Anforderungs Routingregel für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="0ad63-103">Modifies a request routing rule for an application gateway.</span></span>

## <span data-ttu-id="0ad63-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ad63-104">SYNTAX</span></span>

### <span data-ttu-id="0ad63-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0ad63-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettingsId <String>] [-HttpListenerId <String>]
 [-BackendAddressPoolId <String>] [-UrlPathMapId <String>] [-RewriteRuleSetId <String>]
 [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ad63-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="0ad63-106">SetByResource</span></span>
```
Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway <PSApplicationGateway> -Name <String>
 -RuleType <String> [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ad63-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0ad63-107">DESCRIPTION</span></span>
<span data-ttu-id="0ad63-108">Das Cmdlet " **Satz-AzApplicationGatewayRequestRoutingRule** " ändert eine Anforderungs Routingregel.</span><span class="sxs-lookup"><span data-stu-id="0ad63-108">The **Set-AzApplicationGatewayRequestRoutingRule** cmdlet modifies a request routing rule.</span></span>

## <span data-ttu-id="0ad63-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0ad63-109">EXAMPLES</span></span>

### <span data-ttu-id="0ad63-110">Beispiel 1: Aktualisieren einer Anforderungs Routingregel</span><span class="sxs-lookup"><span data-stu-id="0ad63-110">Example 1: Update a request routing rule</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="0ad63-111">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="0ad63-111">The first command gets the application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="0ad63-112">Mit dem zweiten Befehl wird die Anforderungs Routingregel für das Anwendungsgateway so geändert, dass die in der $Setting-Variable angegebenen http-Einstellungen für das Back-End verwendet werden, ein in der $Listener-Variable festgelegter http-Listener und ein in der $Pool-Variable festgelegter Back-End-Adresspool.</span><span class="sxs-lookup"><span data-stu-id="0ad63-112">The second command modifies the request routing rule for the application gateway to use back-end HTTP settings specified in the $Setting variable, an HTTP listener specified in the $Listener variable, and a back-end address pool specified in the $Pool variable.</span></span>

## <span data-ttu-id="0ad63-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ad63-113">PARAMETERS</span></span>

### <span data-ttu-id="0ad63-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0ad63-114">-ApplicationGateway</span></span>
<span data-ttu-id="0ad63-115">Gibt das Application Gateway-Objekt an, mit dem dieses Cmdlet eine Anforderungs Routingregel anordnet.</span><span class="sxs-lookup"><span data-stu-id="0ad63-115">Specifies the application gateway object with which this cmdlet associates a request routing rule.</span></span>

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

### <span data-ttu-id="0ad63-116">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="0ad63-116">-BackendAddressPool</span></span>
<span data-ttu-id="0ad63-117">Gibt den Back-End-Adresspool des Anwendungs Gateways an.</span><span class="sxs-lookup"><span data-stu-id="0ad63-117">Specifies the application gateway back-end address pool.</span></span>

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

### <span data-ttu-id="0ad63-118">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="0ad63-118">-BackendAddressPoolId</span></span>
<span data-ttu-id="0ad63-119">Gibt die ID des Back-End-Adresspools des Anwendungs Gateways an.</span><span class="sxs-lookup"><span data-stu-id="0ad63-119">Specifies the application gateway back-end address pool ID.</span></span>

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

### <span data-ttu-id="0ad63-120">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="0ad63-120">-BackendHttpSettings</span></span>
<span data-ttu-id="0ad63-121">Gibt die http-Einstellungen des Application Gateway-Back-Ends an.</span><span class="sxs-lookup"><span data-stu-id="0ad63-121">Specifies the application gateway backend HTTP settings.</span></span>

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

### <span data-ttu-id="0ad63-122">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="0ad63-122">-BackendHttpSettingsId</span></span>
<span data-ttu-id="0ad63-123">Gibt die ID des Back-End-HTTP-Einstellungen des Anwendungs Gateways an.</span><span class="sxs-lookup"><span data-stu-id="0ad63-123">Specifies the application gateway back-end HTTP settings ID.</span></span>

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

### <span data-ttu-id="0ad63-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ad63-124">-DefaultProfile</span></span>
<span data-ttu-id="0ad63-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0ad63-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ad63-126">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="0ad63-126">-HttpListener</span></span>
<span data-ttu-id="0ad63-127">Gibt den Application Gateway http-Listener an.</span><span class="sxs-lookup"><span data-stu-id="0ad63-127">Specifies the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="0ad63-128">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="0ad63-128">-HttpListenerId</span></span>
<span data-ttu-id="0ad63-129">Gibt die HTTP-Listener-ID des Application Gateway an.</span><span class="sxs-lookup"><span data-stu-id="0ad63-129">Specifies the application gateway HTTP listener ID.</span></span>

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

### <span data-ttu-id="0ad63-130">-Name</span><span class="sxs-lookup"><span data-stu-id="0ad63-130">-Name</span></span>
<span data-ttu-id="0ad63-131">Gibt den Namen der Anforderungs Routingregel an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="0ad63-131">Specifies the name of the request routing rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0ad63-132">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="0ad63-132">-RedirectConfiguration</span></span>
<span data-ttu-id="0ad63-133">Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="0ad63-133">Application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="0ad63-134">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="0ad63-134">-RedirectConfigurationId</span></span>
<span data-ttu-id="0ad63-135">ID des Application Gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="0ad63-135">ID of the application gateway RedirectConfiguration</span></span>

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

### <span data-ttu-id="0ad63-136">-RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0ad63-136">-RewriteRuleSet</span></span>
<span data-ttu-id="0ad63-137">Application Gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0ad63-137">Application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="0ad63-138">-RewriteRuleSetId</span><span class="sxs-lookup"><span data-stu-id="0ad63-138">-RewriteRuleSetId</span></span>
<span data-ttu-id="0ad63-139">ID des Application Gateway RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0ad63-139">ID of the application gateway RewriteRuleSet</span></span>

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

### <span data-ttu-id="0ad63-140">-RuleType</span><span class="sxs-lookup"><span data-stu-id="0ad63-140">-RuleType</span></span>
<span data-ttu-id="0ad63-141">Gibt den Typ der Anforderungs Routingregel an.</span><span class="sxs-lookup"><span data-stu-id="0ad63-141">Specifies the type of request routing rule.</span></span>

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

### <span data-ttu-id="0ad63-142">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="0ad63-142">-UrlPathMap</span></span>
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

### <span data-ttu-id="0ad63-143">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="0ad63-143">-UrlPathMapId</span></span>
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

### <span data-ttu-id="0ad63-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ad63-144">CommonParameters</span></span>
<span data-ttu-id="0ad63-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ad63-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ad63-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ad63-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ad63-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0ad63-147">INPUTS</span></span>

### <span data-ttu-id="0ad63-148">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0ad63-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0ad63-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0ad63-149">OUTPUTS</span></span>

### <span data-ttu-id="0ad63-150">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0ad63-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0ad63-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="0ad63-151">NOTES</span></span>

## <span data-ttu-id="0ad63-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0ad63-152">RELATED LINKS</span></span>

[<span data-ttu-id="0ad63-153">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0ad63-153">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="0ad63-154">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0ad63-154">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="0ad63-155">Neu – AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0ad63-155">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="0ad63-156">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0ad63-156">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)


