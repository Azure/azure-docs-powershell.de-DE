---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: d3434a650eb09391aa7505f288667aa130401e26
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175469"
---
# <span data-ttu-id="c2539-101">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c2539-101">Add-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="c2539-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c2539-102">SYNOPSIS</span></span>
<span data-ttu-id="c2539-103">Fügt einen HTTP-Listener zu einem Anwendungsgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="c2539-103">Adds an HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="c2539-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2539-104">SYNTAX</span></span>

### <span data-ttu-id="c2539-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c2539-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-FirewallPolicyId <String>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2539-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c2539-106">SetByResource</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c2539-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2539-107">DESCRIPTION</span></span>
<span data-ttu-id="c2539-108">Mit dem Cmdlet **Add-AzApplicationGatewayHttpListener** wird ein HTTP-Listener zu einem Anwendungsgateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c2539-108">The **Add-AzApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="c2539-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c2539-109">EXAMPLES</span></span>

### <span data-ttu-id="c2539-110">Beispiel 1: Hinzufügen eines HTTP-Listeners</span><span class="sxs-lookup"><span data-stu-id="c2539-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="c2539-111">Der erste Befehl ruft das Anwendungsgateway ab und speichert es in der $AppGw-Variablen. Mit dem zweiten Befehl wird der HTTP-Listener dem Anwendungsgateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c2539-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="c2539-112">Beispiel 2: Hinzufügen eines HTTPS-Listener mit SSL</span><span class="sxs-lookup"><span data-stu-id="c2539-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="c2539-113">Der erste Befehl ruft das Anwendungsgateway ab und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="c2539-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c2539-114">Mit dem zweiten Befehl wird der Listener, der das HTTPS-Protokoll verwendet, zum Anwendungsgateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c2539-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

### <span data-ttu-id="c2539-115">Beispiel 3: Hinzufügen eines HTTPS-Listener mit SSL und Hostnamen</span><span class="sxs-lookup"><span data-stu-id="c2539-115">Example 3: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="c2539-116">Der erste Befehl ruft das Anwendungsgateway ab und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="c2539-116">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c2539-117">Mit dem zweiten Befehl wird der Listener, der das HTTPS-Protokoll verwendet, mit SSL-Zertifikaten und-Hostnamen zum Anwendungsgateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c2539-117">The second command adds the listener, which uses the HTTPS protocol, with SSL Certificates and HostNames, to the application gateway.</span></span>

## <span data-ttu-id="c2539-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2539-118">PARAMETERS</span></span>

### <span data-ttu-id="c2539-119">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c2539-119">-ApplicationGateway</span></span>
<span data-ttu-id="c2539-120">Gibt das Anwendungsgateway an, dem dieses Cmdlet einen HTTP-Listener hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="c2539-120">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

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

### <span data-ttu-id="c2539-121">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2539-121">-CustomErrorConfiguration</span></span>
<span data-ttu-id="c2539-122">Kunden Fehler eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="c2539-122">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="c2539-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2539-123">-DefaultProfile</span></span>
<span data-ttu-id="c2539-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c2539-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2539-125">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="c2539-125">-FirewallPolicy</span></span>
<span data-ttu-id="c2539-126">FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="c2539-126">FirewallPolicy</span></span>

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

### <span data-ttu-id="c2539-127">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="c2539-127">-FirewallPolicyId</span></span>
<span data-ttu-id="c2539-128">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="c2539-128">FirewallPolicyId</span></span>

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

### <span data-ttu-id="c2539-129">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2539-129">-FrontendIPConfiguration</span></span>
<span data-ttu-id="c2539-130">Gibt das Front-End-IP-Ressourcenobjekt des Application Gateway an.</span><span class="sxs-lookup"><span data-stu-id="c2539-130">Specifies the application gateway front-end IP resource object.</span></span>

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

### <span data-ttu-id="c2539-131">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="c2539-131">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="c2539-132">Gibt die Front-End-IP-ID des Application Gateway an.</span><span class="sxs-lookup"><span data-stu-id="c2539-132">Specifies the application gateway front-end IP ID.</span></span>

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

### <span data-ttu-id="c2539-133">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="c2539-133">-FrontendPort</span></span>
<span data-ttu-id="c2539-134">Gibt das Front-End-Port Objekt des Application Gateway an.</span><span class="sxs-lookup"><span data-stu-id="c2539-134">Specifies the application gateway front-end port object.</span></span>

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

### <span data-ttu-id="c2539-135">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="c2539-135">-FrontendPortId</span></span>
<span data-ttu-id="c2539-136">Gibt die Front-End-Port-ID des Application Gateway an.</span><span class="sxs-lookup"><span data-stu-id="c2539-136">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="c2539-137">-Hostname</span><span class="sxs-lookup"><span data-stu-id="c2539-137">-HostName</span></span>
<span data-ttu-id="c2539-138">Gibt den Hostnamen an, dem dieses Cmdlet einen HTTP-Listener hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="c2539-138">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

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

### <span data-ttu-id="c2539-139">-Hostnames</span><span class="sxs-lookup"><span data-stu-id="c2539-139">-HostNames</span></span>
<span data-ttu-id="c2539-140">Hostnamen</span><span class="sxs-lookup"><span data-stu-id="c2539-140">Host names</span></span>

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

### <span data-ttu-id="c2539-141">-Name</span><span class="sxs-lookup"><span data-stu-id="c2539-141">-Name</span></span>
<span data-ttu-id="c2539-142">Gibt den Namen des Front-End-Ports an, den dieser Befehl hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="c2539-142">Specifies the name of the front-end port that this command adds.</span></span>

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

### <span data-ttu-id="c2539-143">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="c2539-143">-Protocol</span></span>
<span data-ttu-id="c2539-144">Gibt das Protokoll des HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="c2539-144">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="c2539-145">Sowohl HTTP als auch HTTPS werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c2539-145">Both HTTP and HTTPS are supported.</span></span>

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

### <span data-ttu-id="c2539-146">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="c2539-146">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="c2539-147">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="c2539-147">-SslCertificate</span></span>
<span data-ttu-id="c2539-148">Gibt das SSL-Zertifikat des HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="c2539-148">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="c2539-149">Muss angegeben werden, wenn HTTPS als Listener-Protokoll ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="c2539-149">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="c2539-150">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="c2539-150">-SslCertificateId</span></span>
<span data-ttu-id="c2539-151">Gibt die SSL-Zertifikat-ID des HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="c2539-151">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="c2539-152">Muss angegeben werden, wenn HTTPS als Listener-Protokoll ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="c2539-152">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="c2539-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2539-153">CommonParameters</span></span>
<span data-ttu-id="c2539-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2539-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2539-155">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2539-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2539-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c2539-156">INPUTS</span></span>

### <span data-ttu-id="c2539-157">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c2539-157">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c2539-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c2539-158">OUTPUTS</span></span>

### <span data-ttu-id="c2539-159">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c2539-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c2539-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="c2539-160">NOTES</span></span>

## <span data-ttu-id="c2539-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c2539-161">RELATED LINKS</span></span>

[<span data-ttu-id="c2539-162">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c2539-162">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="c2539-163">Neu – AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c2539-163">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="c2539-164">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c2539-164">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="c2539-165">Satz-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c2539-165">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


