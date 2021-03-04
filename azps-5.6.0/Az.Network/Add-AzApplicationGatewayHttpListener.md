---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 51d85ffa9c1181b45f7ea4aa45484a814759a953
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933931"
---
# <span data-ttu-id="b829b-101">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b829b-101">Add-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="b829b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b829b-102">SYNOPSIS</span></span>
<span data-ttu-id="b829b-103">Fügt einem Anwendungsgateway einen HTTP-Listener hinzu.</span><span class="sxs-lookup"><span data-stu-id="b829b-103">Adds an HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="b829b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b829b-104">SYNTAX</span></span>

### <span data-ttu-id="b829b-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="b829b-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-FirewallPolicyId <String>] [-SslProfileId <String>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b829b-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b829b-106">SetByResource</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-SslProfile <PSApplicationGatewaySslProfile>]
 [-HostName <String>] [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b829b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b829b-107">DESCRIPTION</span></span>
<span data-ttu-id="b829b-108">Das **Add-AzApplicationGatewayHttpListener-Cmdlet** fügt einem Anwendungsgateway einen HTTP-Listener hinzu.</span><span class="sxs-lookup"><span data-stu-id="b829b-108">The **Add-AzApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="b829b-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b829b-109">EXAMPLES</span></span>

### <span data-ttu-id="b829b-110">Beispiel 1: Hinzufügen eines HTTP-Listeners</span><span class="sxs-lookup"><span data-stu-id="b829b-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="b829b-111">Der erste Befehl ruft das Anwendungsgateway ab und speichert es in der $AppGw Variablen. Mit dem zweiten Befehl wird der HTTP-Listener zum Anwendungsgateway addiert.</span><span class="sxs-lookup"><span data-stu-id="b829b-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="b829b-112">Beispiel 2: Hinzufügen eines HTTPS-Listeners mit SSL</span><span class="sxs-lookup"><span data-stu-id="b829b-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="b829b-113">Der erste Befehl ruft das Anwendungsgateway ab und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="b829b-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b829b-114">Der zweite Befehl fügt den Listener, der das HTTPS-Protokoll verwendet, zum Anwendungsgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="b829b-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

### <span data-ttu-id="b829b-115">Beispiel 3: Hinzufügen eines HTTPS-Listeners mit SSL und HostNamen</span><span class="sxs-lookup"><span data-stu-id="b829b-115">Example 3: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com","www.microsoft.com"
```

<span data-ttu-id="b829b-116">Der erste Befehl ruft das Anwendungsgateway ab und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="b829b-116">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b829b-117">Mit dem zweiten Befehl wird der Listener, der das HTTPS-Protokoll mit SSL-Zertifikaten und HostNamen verwendet, zum Anwendungsgateway addiert.</span><span class="sxs-lookup"><span data-stu-id="b829b-117">The second command adds the listener, which uses the HTTPS protocol, with SSL Certificates and HostNames, to the application gateway.</span></span>

## <span data-ttu-id="b829b-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b829b-118">PARAMETERS</span></span>

### <span data-ttu-id="b829b-119">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b829b-119">-ApplicationGateway</span></span>
<span data-ttu-id="b829b-120">Gibt das Anwendungsgateway an, dem dieses Cmdlet einen HTTP-Listener hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="b829b-120">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

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

### <span data-ttu-id="b829b-121">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="b829b-121">-CustomErrorConfiguration</span></span>
<span data-ttu-id="b829b-122">Kundenfehler eines Anwendungsgateways</span><span class="sxs-lookup"><span data-stu-id="b829b-122">Customer error of an application gateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b829b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b829b-123">-DefaultProfile</span></span>
<span data-ttu-id="b829b-124">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b829b-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b829b-125">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="b829b-125">-FirewallPolicy</span></span>
<span data-ttu-id="b829b-126">FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="b829b-126">FirewallPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b829b-127">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="b829b-127">-FirewallPolicyId</span></span>
<span data-ttu-id="b829b-128">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="b829b-128">FirewallPolicyId</span></span>

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

### <span data-ttu-id="b829b-129">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b829b-129">-FrontendIPConfiguration</span></span>
<span data-ttu-id="b829b-130">Gibt das Front-End-IP-Ressourcenobjekt des Anwendungsgateways an.</span><span class="sxs-lookup"><span data-stu-id="b829b-130">Specifies the application gateway front-end IP resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b829b-131">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b829b-131">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="b829b-132">Gibt die Front-End-IP-ID des Anwendungsgateways an.</span><span class="sxs-lookup"><span data-stu-id="b829b-132">Specifies the application gateway front-end IP ID.</span></span>

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

### <span data-ttu-id="b829b-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="b829b-133">-FrontendPort</span></span>
<span data-ttu-id="b829b-134">Gibt das Front-End-Portobjekt des Anwendungsgateways an.</span><span class="sxs-lookup"><span data-stu-id="b829b-134">Specifies the application gateway front-end port object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b829b-135">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="b829b-135">-FrontendPortId</span></span>
<span data-ttu-id="b829b-136">Gibt die Front-End-Port-ID des Anwendungsgateways an.</span><span class="sxs-lookup"><span data-stu-id="b829b-136">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="b829b-137">-HostName</span><span class="sxs-lookup"><span data-stu-id="b829b-137">-HostName</span></span>
<span data-ttu-id="b829b-138">Gibt den Hostnamen an, dem dieses Cmdlet einen HTTP-Listener hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="b829b-138">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b829b-139">-HostNames</span><span class="sxs-lookup"><span data-stu-id="b829b-139">-HostNames</span></span>
<span data-ttu-id="b829b-140">Hostnamen</span><span class="sxs-lookup"><span data-stu-id="b829b-140">Host names</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b829b-141">-Name</span><span class="sxs-lookup"><span data-stu-id="b829b-141">-Name</span></span>
<span data-ttu-id="b829b-142">Gibt den Namen des Front-End-Ports an, den dieser Befehl hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="b829b-142">Specifies the name of the front-end port that this command adds.</span></span>

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

### <span data-ttu-id="b829b-143">-Protocol</span><span class="sxs-lookup"><span data-stu-id="b829b-143">-Protocol</span></span>
<span data-ttu-id="b829b-144">Gibt das Protokoll des HTTP-Listeners an.</span><span class="sxs-lookup"><span data-stu-id="b829b-144">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="b829b-145">Sowohl HTTP als auch HTTPS werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b829b-145">Both HTTP and HTTPS are supported.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b829b-146">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="b829b-146">-RequireServerNameIndication</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: true, false

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b829b-147">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="b829b-147">-SslCertificate</span></span>
<span data-ttu-id="b829b-148">Gibt das SSL-Zertifikat des HTTP-Listeners an.</span><span class="sxs-lookup"><span data-stu-id="b829b-148">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="b829b-149">Muss angegeben werden, wenn HTTPS als Listenerprotokoll ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="b829b-149">Must be specified if HTTPS is chosen as listener protocol.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b829b-150">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="b829b-150">-SslCertificateId</span></span>
<span data-ttu-id="b829b-151">Gibt die SSL-Zertifikat-ID des HTTP-Listeners an.</span><span class="sxs-lookup"><span data-stu-id="b829b-151">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="b829b-152">Muss angegeben werden, wenn HTTPS als Listenerprotokoll ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="b829b-152">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="b829b-153">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="b829b-153">-SslProfile</span></span>
<span data-ttu-id="b829b-154">SslProfile</span><span class="sxs-lookup"><span data-stu-id="b829b-154">SslProfile</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b829b-155">-SslProfileId</span><span class="sxs-lookup"><span data-stu-id="b829b-155">-SslProfileId</span></span>
<span data-ttu-id="b829b-156">SslProfileId</span><span class="sxs-lookup"><span data-stu-id="b829b-156">SslProfileId</span></span>

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

### <span data-ttu-id="b829b-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b829b-157">CommonParameters</span></span>
<span data-ttu-id="b829b-158">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b829b-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b829b-159">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b829b-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b829b-160">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b829b-160">INPUTS</span></span>

### <span data-ttu-id="b829b-161">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b829b-161">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b829b-162">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b829b-162">OUTPUTS</span></span>

### <span data-ttu-id="b829b-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b829b-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b829b-164">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b829b-164">NOTES</span></span>

## <span data-ttu-id="b829b-165">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b829b-165">RELATED LINKS</span></span>

[<span data-ttu-id="b829b-166">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b829b-166">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="b829b-167">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b829b-167">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="b829b-168">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b829b-168">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="b829b-169">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b829b-169">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


