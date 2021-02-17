---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 8ce5d01d78b8b434e062b0f33ee41a4cbbce20ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156785"
---
# <span data-ttu-id="6f872-101">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6f872-101">Set-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="6f872-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f872-102">SYNOPSIS</span></span>
<span data-ttu-id="6f872-103">Ändert einen HTTP-Listener für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="6f872-103">Modifies an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="6f872-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6f872-104">SYNTAX</span></span>

### <span data-ttu-id="6f872-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="6f872-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-FirewallPolicyId <String>] [-SslProfileId <String>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6f872-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="6f872-106">SetByResource</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-SslProfile <PSApplicationGatewaySslProfile>]
 [-HostName <String>] [-HostNames <String[]>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6f872-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6f872-107">DESCRIPTION</span></span>
<span data-ttu-id="6f872-108">Das **Cmdlet "Set-AzApplicationGatewayHttpListener"** ändert einen HTTP-Listener für ein Azure-Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="6f872-108">The **Set-AzApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="6f872-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6f872-109">EXAMPLES</span></span>

### <span data-ttu-id="6f872-110">Beispiel 1: Festlegen eines HTTP-Listeners</span><span class="sxs-lookup"><span data-stu-id="6f872-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="6f872-111">Der erste Befehl ruft das Anwendungsgateway namens ApplicationGateway01 ab, das zur Ressourcengruppe "ResourceGroup01" gehört, und speichert es in der $AppGw Variable.</span><span class="sxs-lookup"><span data-stu-id="6f872-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="6f872-112">Mit dem zweiten Befehl wird der HTTP-Listener für das Gateway so konfiguriert, dass die front-end-Konfiguration verwendet wird, die in $FIP 01 mit dem HTTP-Protokoll auf Port 80 gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="6f872-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

### <span data-ttu-id="6f872-113">Beispiel 2: Hinzufügen eines HTTPS-Listeners mit SSL und HostNames</span><span class="sxs-lookup"><span data-stu-id="6f872-113">Example 2: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="6f872-114">Der erste Befehl ruft das Anwendungsgateway ab und speichert es in der $AppGw Variable.</span><span class="sxs-lookup"><span data-stu-id="6f872-114">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="6f872-115">Mit dem zweiten Befehl wird der Listener, der das HTTPS-Protokoll verwendet, mit SSL-Zertifikaten und Hostnamen, dem Anwendungsgateway hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="6f872-115">The second command adds the listener, which uses the HTTPS protocol, with SSL Certificates and HostNames, to the application gateway.</span></span>

## <span data-ttu-id="6f872-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f872-116">PARAMETERS</span></span>

### <span data-ttu-id="6f872-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6f872-117">-ApplicationGateway</span></span>
<span data-ttu-id="6f872-118">Gibt das Anwendungsgateway an, dem dieses Cmdlet den HTTP-Listener zu ordnet.</span><span class="sxs-lookup"><span data-stu-id="6f872-118">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="6f872-119">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="6f872-119">-CustomErrorConfiguration</span></span>
<span data-ttu-id="6f872-120">Kundenfehler eines Anwendungsgateways</span><span class="sxs-lookup"><span data-stu-id="6f872-120">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="6f872-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f872-121">-DefaultProfile</span></span>
<span data-ttu-id="6f872-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6f872-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f872-123">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="6f872-123">-FirewallPolicy</span></span>
<span data-ttu-id="6f872-124">FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="6f872-124">FirewallPolicy</span></span>

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

### <span data-ttu-id="6f872-125">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="6f872-125">-FirewallPolicyId</span></span>
<span data-ttu-id="6f872-126">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="6f872-126">FirewallPolicyId</span></span>

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

### <span data-ttu-id="6f872-127">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="6f872-127">-FrontendIPConfiguration</span></span>
<span data-ttu-id="6f872-128">Gibt die Front-End-IP-Adresse des Anwendungsgateways an.</span><span class="sxs-lookup"><span data-stu-id="6f872-128">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="6f872-129">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6f872-129">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="6f872-130">Gibt die ID der Front-End-IP-Adresse des Anwendungsgateways an.</span><span class="sxs-lookup"><span data-stu-id="6f872-130">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="6f872-131">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="6f872-131">-FrontendPort</span></span>
<span data-ttu-id="6f872-132">Gibt den Front-End-Port des Anwendungsgateways an.</span><span class="sxs-lookup"><span data-stu-id="6f872-132">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="6f872-133">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="6f872-133">-FrontendPortId</span></span>
<span data-ttu-id="6f872-134">Gibt die Front-End-Port-ID des Anwendungsgateways an.</span><span class="sxs-lookup"><span data-stu-id="6f872-134">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="6f872-135">-HostName</span><span class="sxs-lookup"><span data-stu-id="6f872-135">-HostName</span></span>
<span data-ttu-id="6f872-136">Gibt den Hostnamen an, an den dieses Cmdlet den HTTP-Listener sendet.</span><span class="sxs-lookup"><span data-stu-id="6f872-136">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="6f872-137">-HostNames</span><span class="sxs-lookup"><span data-stu-id="6f872-137">-HostNames</span></span>
<span data-ttu-id="6f872-138">Hostnamen</span><span class="sxs-lookup"><span data-stu-id="6f872-138">Host names</span></span>

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

### <span data-ttu-id="6f872-139">-Name</span><span class="sxs-lookup"><span data-stu-id="6f872-139">-Name</span></span>
<span data-ttu-id="6f872-140">Gibt den Namen des HTTP-Listeners an.</span><span class="sxs-lookup"><span data-stu-id="6f872-140">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="6f872-141">-Protocol</span><span class="sxs-lookup"><span data-stu-id="6f872-141">-Protocol</span></span>
<span data-ttu-id="6f872-142">Gibt das Protokoll an, das vom HTTP-Listener verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6f872-142">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="6f872-143">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="6f872-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6f872-144">Http</span><span class="sxs-lookup"><span data-stu-id="6f872-144">Http</span></span>
- <span data-ttu-id="6f872-145">Https</span><span class="sxs-lookup"><span data-stu-id="6f872-145">Https</span></span>

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

### <span data-ttu-id="6f872-146">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="6f872-146">-RequireServerNameIndication</span></span>
<span data-ttu-id="6f872-147">Gibt an, ob für das Cmdlet eine Servernamensanzeige erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="6f872-147">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="6f872-148">Die zulässigen Werte für diesen Parameter sind" true" oder "false".</span><span class="sxs-lookup"><span data-stu-id="6f872-148">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="6f872-149">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="6f872-149">-SslCertificate</span></span>
<span data-ttu-id="6f872-150">Gibt das SSL-Zertifikat des HTTP-Listeners an.</span><span class="sxs-lookup"><span data-stu-id="6f872-150">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="6f872-151">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="6f872-151">-SslCertificateId</span></span>
<span data-ttu-id="6f872-152">Gibt die SSL-Zertifikat-ID (Secure Socket Layer) des HTTP-Listeners an.</span><span class="sxs-lookup"><span data-stu-id="6f872-152">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="6f872-153">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="6f872-153">-SslProfile</span></span>
<span data-ttu-id="6f872-154">SslProfile</span><span class="sxs-lookup"><span data-stu-id="6f872-154">SslProfile</span></span>

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

### <span data-ttu-id="6f872-155">-SslProfileId</span><span class="sxs-lookup"><span data-stu-id="6f872-155">-SslProfileId</span></span>
<span data-ttu-id="6f872-156">SslProfileId</span><span class="sxs-lookup"><span data-stu-id="6f872-156">SslProfileId</span></span>

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

### <span data-ttu-id="6f872-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f872-157">CommonParameters</span></span>
<span data-ttu-id="6f872-158">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f872-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f872-159">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6f872-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f872-160">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6f872-160">INPUTS</span></span>

### <span data-ttu-id="6f872-161">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6f872-161">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6f872-162">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6f872-162">OUTPUTS</span></span>

### <span data-ttu-id="6f872-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6f872-163">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6f872-164">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6f872-164">NOTES</span></span>

## <span data-ttu-id="6f872-165">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6f872-165">RELATED LINKS</span></span>

[<span data-ttu-id="6f872-166">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6f872-166">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="6f872-167">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6f872-167">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="6f872-168">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6f872-168">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="6f872-169">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="6f872-169">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)


