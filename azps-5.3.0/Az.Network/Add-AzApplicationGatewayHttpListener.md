---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: f769eb91d524bc9115199127833471246f6fdd1f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380315"
---
# <span data-ttu-id="bec87-101">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="bec87-101">Add-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="bec87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bec87-102">SYNOPSIS</span></span>
<span data-ttu-id="bec87-103">Fügt einem Anwendungsgateway einen HTTP-Listener hinzu.</span><span class="sxs-lookup"><span data-stu-id="bec87-103">Adds an HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="bec87-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bec87-104">SYNTAX</span></span>

### <span data-ttu-id="bec87-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="bec87-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-FirewallPolicyId <String>] [-SslProfileId <String>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bec87-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="bec87-106">SetByResource</span></span>
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

## <span data-ttu-id="bec87-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bec87-107">DESCRIPTION</span></span>
<span data-ttu-id="bec87-108">Das **Cmdlet "Add-AzApplicationGatewayHttpListener"** fügt einem Anwendungsgateway einen HTTP-Listener hinzu.</span><span class="sxs-lookup"><span data-stu-id="bec87-108">The **Add-AzApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="bec87-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bec87-109">EXAMPLES</span></span>

### <span data-ttu-id="bec87-110">Beispiel 1: Hinzufügen eines HTTP-Listeners</span><span class="sxs-lookup"><span data-stu-id="bec87-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="bec87-111">Der erste Befehl ruft das Anwendungsgateway ab und speichert es in der $AppGw Variable. Mit dem zweiten Befehl wird der HTTP-Listener dem Anwendungsgateway hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="bec87-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="bec87-112">Beispiel 2: Hinzufügen eines HTTPS-Listeners mit SSL</span><span class="sxs-lookup"><span data-stu-id="bec87-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="bec87-113">Der erste Befehl ruft das Anwendungsgateway ab und speichert es in der $AppGw Variable.</span><span class="sxs-lookup"><span data-stu-id="bec87-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="bec87-114">Der zweite Befehl fügt den Listener, der das HTTPS-Protokoll verwendet, dem Anwendungsgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="bec87-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

### <span data-ttu-id="bec87-115">Beispiel 3: Hinzufügen eines HTTPS-Listeners mit SSL und HostNames</span><span class="sxs-lookup"><span data-stu-id="bec87-115">Example 3: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com","www.microsoft.com"
```

<span data-ttu-id="bec87-116">Der erste Befehl ruft das Anwendungsgateway ab und speichert es in der $AppGw Variable.</span><span class="sxs-lookup"><span data-stu-id="bec87-116">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="bec87-117">Der zweite Befehl fügt den Listener, der das HTTPS-Protokoll verwendet, mit SSL-Zertifikaten und Hostnamen, zum Anwendungsgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="bec87-117">The second command adds the listener, which uses the HTTPS protocol, with SSL Certificates and HostNames, to the application gateway.</span></span>

## <span data-ttu-id="bec87-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bec87-118">PARAMETERS</span></span>

### <span data-ttu-id="bec87-119">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bec87-119">-ApplicationGateway</span></span>
<span data-ttu-id="bec87-120">Gibt das Anwendungsgateway an, dem dieses Cmdlet einen HTTP-Listener hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="bec87-120">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

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

### <span data-ttu-id="bec87-121">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="bec87-121">-CustomErrorConfiguration</span></span>
<span data-ttu-id="bec87-122">Kundenfehler eines Anwendungsgateways</span><span class="sxs-lookup"><span data-stu-id="bec87-122">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="bec87-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bec87-123">-DefaultProfile</span></span>
<span data-ttu-id="bec87-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bec87-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bec87-125">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="bec87-125">-FirewallPolicy</span></span>
<span data-ttu-id="bec87-126">FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="bec87-126">FirewallPolicy</span></span>

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

### <span data-ttu-id="bec87-127">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="bec87-127">-FirewallPolicyId</span></span>
<span data-ttu-id="bec87-128">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="bec87-128">FirewallPolicyId</span></span>

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

### <span data-ttu-id="bec87-129">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="bec87-129">-FrontendIPConfiguration</span></span>
<span data-ttu-id="bec87-130">Gibt das Front-End-IP-Ressourcenobjekt des Anwendungsgateways an.</span><span class="sxs-lookup"><span data-stu-id="bec87-130">Specifies the application gateway front-end IP resource object.</span></span>

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

### <span data-ttu-id="bec87-131">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="bec87-131">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="bec87-132">Gibt die Front-End-IP-ID des Anwendungsgateways an.</span><span class="sxs-lookup"><span data-stu-id="bec87-132">Specifies the application gateway front-end IP ID.</span></span>

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

### <span data-ttu-id="bec87-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="bec87-133">-FrontendPort</span></span>
<span data-ttu-id="bec87-134">Gibt das Front-End-Portobjekt des Anwendungsgateways an.</span><span class="sxs-lookup"><span data-stu-id="bec87-134">Specifies the application gateway front-end port object.</span></span>

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

### <span data-ttu-id="bec87-135">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="bec87-135">-FrontendPortId</span></span>
<span data-ttu-id="bec87-136">Gibt die Front-End-Port-ID des Anwendungsgateways an.</span><span class="sxs-lookup"><span data-stu-id="bec87-136">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="bec87-137">-HostName</span><span class="sxs-lookup"><span data-stu-id="bec87-137">-HostName</span></span>
<span data-ttu-id="bec87-138">Gibt den Hostnamen an, dem dieses Cmdlet einen HTTP-Listener hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="bec87-138">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

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

### <span data-ttu-id="bec87-139">-HostNames</span><span class="sxs-lookup"><span data-stu-id="bec87-139">-HostNames</span></span>
<span data-ttu-id="bec87-140">Hostnamen</span><span class="sxs-lookup"><span data-stu-id="bec87-140">Host names</span></span>

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

### <span data-ttu-id="bec87-141">-Name</span><span class="sxs-lookup"><span data-stu-id="bec87-141">-Name</span></span>
<span data-ttu-id="bec87-142">Gibt den Namen des Front-End-Ports an, den dieser Befehl hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="bec87-142">Specifies the name of the front-end port that this command adds.</span></span>

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

### <span data-ttu-id="bec87-143">-Protocol</span><span class="sxs-lookup"><span data-stu-id="bec87-143">-Protocol</span></span>
<span data-ttu-id="bec87-144">Gibt das Protokoll des HTTP-Listeners an.</span><span class="sxs-lookup"><span data-stu-id="bec87-144">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="bec87-145">SOWOHL HTTP als auch HTTPS werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bec87-145">Both HTTP and HTTPS are supported.</span></span>

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

### <span data-ttu-id="bec87-146">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="bec87-146">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="bec87-147">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="bec87-147">-SslCertificate</span></span>
<span data-ttu-id="bec87-148">Gibt das SSL-Zertifikat des HTTP-Listeners an.</span><span class="sxs-lookup"><span data-stu-id="bec87-148">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="bec87-149">Muss angegeben werden, wenn HTTPS als Listenerprotokoll ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="bec87-149">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="bec87-150">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="bec87-150">-SslCertificateId</span></span>
<span data-ttu-id="bec87-151">Gibt die SSL-Zertifikat-ID des HTTP-Listeners an.</span><span class="sxs-lookup"><span data-stu-id="bec87-151">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="bec87-152">Muss angegeben werden, wenn HTTPS als Listenerprotokoll ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="bec87-152">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="bec87-153">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="bec87-153">-SslProfile</span></span>
<span data-ttu-id="bec87-154">SslProfile</span><span class="sxs-lookup"><span data-stu-id="bec87-154">SslProfile</span></span>

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

### <span data-ttu-id="bec87-155">-SslProfileId</span><span class="sxs-lookup"><span data-stu-id="bec87-155">-SslProfileId</span></span>
<span data-ttu-id="bec87-156">SslProfileId</span><span class="sxs-lookup"><span data-stu-id="bec87-156">SslProfileId</span></span>

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

### <span data-ttu-id="bec87-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bec87-157">CommonParameters</span></span>
<span data-ttu-id="bec87-158">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bec87-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bec87-159">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bec87-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bec87-160">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bec87-160">INPUTS</span></span>

### <span data-ttu-id="bec87-161">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bec87-161">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bec87-162">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bec87-162">OUTPUTS</span></span>

### <span data-ttu-id="bec87-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bec87-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bec87-164">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bec87-164">NOTES</span></span>

## <span data-ttu-id="bec87-165">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bec87-165">RELATED LINKS</span></span>

[<span data-ttu-id="bec87-166">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="bec87-166">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="bec87-167">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="bec87-167">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="bec87-168">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="bec87-168">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="bec87-169">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="bec87-169">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


