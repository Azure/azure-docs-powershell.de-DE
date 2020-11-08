---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 3cc9af0865ca47099f5617cc1e94f3232ed9bdb7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174536"
---
# <span data-ttu-id="a026b-101">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a026b-101">Set-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="a026b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a026b-102">SYNOPSIS</span></span>
<span data-ttu-id="a026b-103">Ändert einen HTTP-Listener für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="a026b-103">Modifies an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="a026b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a026b-104">SYNTAX</span></span>

### <span data-ttu-id="a026b-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a026b-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-FirewallPolicyId <String>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a026b-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="a026b-106">SetByResource</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>]
 [-FirewallPolicy <PSApplicationGatewayWebApplicationFirewallPolicy>]
 [-SslCertificate <PSApplicationGatewaySslCertificate>] [-HostName <String>] [-HostNames <String[]>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a026b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a026b-107">DESCRIPTION</span></span>
<span data-ttu-id="a026b-108">Das Cmdlet " **Satz-AzApplicationGatewayHttpListener** " ändert einen HTTP-Listener für ein Azure Application-Gateway.</span><span class="sxs-lookup"><span data-stu-id="a026b-108">The **Set-AzApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="a026b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a026b-109">EXAMPLES</span></span>

### <span data-ttu-id="a026b-110">Beispiel 1: Einrichten eines HTTP-Listener</span><span class="sxs-lookup"><span data-stu-id="a026b-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="a026b-111">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="a026b-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a026b-112">Der zweite Befehl legt den HTTP-Listener für das Gateway so fest, dass die in $FIP 01 gespeicherte Front-End-Konfiguration mit dem HTTP-Protokoll auf Port 80 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a026b-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

### <span data-ttu-id="a026b-113">Beispiel 2: Hinzufügen eines HTTPS-Listener mit SSL und Hostnamen</span><span class="sxs-lookup"><span data-stu-id="a026b-113">Example 2: Add a HTTPS listener with SSL and HostNames</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01 -HostNames "*.contoso.com,www.microsoft.com"
```

<span data-ttu-id="a026b-114">Der erste Befehl ruft das Anwendungsgateway ab und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a026b-114">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a026b-115">Mit dem zweiten Befehl wird der Listener, der das HTTPS-Protokoll verwendet, mit SSL-Zertifikaten und-Hostnamen zum Anwendungsgateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a026b-115">The second command adds the listener, which uses the HTTPS protocol, with SSL Certificates and HostNames, to the application gateway.</span></span>

## <span data-ttu-id="a026b-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="a026b-116">PARAMETERS</span></span>

### <span data-ttu-id="a026b-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a026b-117">-ApplicationGateway</span></span>
<span data-ttu-id="a026b-118">Gibt das Anwendungsgateway an, mit dem dieses Cmdlet den HTTP-Listener verknüpft.</span><span class="sxs-lookup"><span data-stu-id="a026b-118">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="a026b-119">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="a026b-119">-CustomErrorConfiguration</span></span>
<span data-ttu-id="a026b-120">Kunden Fehler eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="a026b-120">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="a026b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a026b-121">-DefaultProfile</span></span>
<span data-ttu-id="a026b-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a026b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a026b-123">-FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="a026b-123">-FirewallPolicy</span></span>
<span data-ttu-id="a026b-124">FirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="a026b-124">FirewallPolicy</span></span>

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

### <span data-ttu-id="a026b-125">-FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="a026b-125">-FirewallPolicyId</span></span>
<span data-ttu-id="a026b-126">FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="a026b-126">FirewallPolicyId</span></span>

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

### <span data-ttu-id="a026b-127">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a026b-127">-FrontendIPConfiguration</span></span>
<span data-ttu-id="a026b-128">Gibt die Front-End-IP-Adresse des Anwendungs Gateways an.</span><span class="sxs-lookup"><span data-stu-id="a026b-128">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="a026b-129">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="a026b-129">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="a026b-130">Gibt die ID der Front-End-IP-Adresse des Anwendungs Gateways an.</span><span class="sxs-lookup"><span data-stu-id="a026b-130">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="a026b-131">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="a026b-131">-FrontendPort</span></span>
<span data-ttu-id="a026b-132">Gibt den Front-End-Port des Application Gateway an.</span><span class="sxs-lookup"><span data-stu-id="a026b-132">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="a026b-133">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="a026b-133">-FrontendPortId</span></span>
<span data-ttu-id="a026b-134">Gibt die Front-End-Port-ID des Application Gateway an.</span><span class="sxs-lookup"><span data-stu-id="a026b-134">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="a026b-135">-Hostname</span><span class="sxs-lookup"><span data-stu-id="a026b-135">-HostName</span></span>
<span data-ttu-id="a026b-136">Gibt den Hostnamen an, an den dieses Cmdlet den HTTP-Listener sendet.</span><span class="sxs-lookup"><span data-stu-id="a026b-136">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="a026b-137">-Hostnames</span><span class="sxs-lookup"><span data-stu-id="a026b-137">-HostNames</span></span>
<span data-ttu-id="a026b-138">Hostnamen</span><span class="sxs-lookup"><span data-stu-id="a026b-138">Host names</span></span>

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

### <span data-ttu-id="a026b-139">-Name</span><span class="sxs-lookup"><span data-stu-id="a026b-139">-Name</span></span>
<span data-ttu-id="a026b-140">Gibt den Namen des HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="a026b-140">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="a026b-141">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="a026b-141">-Protocol</span></span>
<span data-ttu-id="a026b-142">Gibt das Protokoll an, das der HTTP-Listener verwendet.</span><span class="sxs-lookup"><span data-stu-id="a026b-142">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="a026b-143">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a026b-143">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a026b-144">Http</span><span class="sxs-lookup"><span data-stu-id="a026b-144">Http</span></span>
- <span data-ttu-id="a026b-145">HTTPS</span><span class="sxs-lookup"><span data-stu-id="a026b-145">Https</span></span>

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

### <span data-ttu-id="a026b-146">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="a026b-146">-RequireServerNameIndication</span></span>
<span data-ttu-id="a026b-147">Gibt an, ob für das Cmdlet eine Servernamen Angabe erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a026b-147">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="a026b-148">Die zulässigen Werte für diesen Parameter lauten: wahr oder falsch.</span><span class="sxs-lookup"><span data-stu-id="a026b-148">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="a026b-149">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="a026b-149">-SslCertificate</span></span>
<span data-ttu-id="a026b-150">Gibt das SSL-Zertifikat des HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="a026b-150">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="a026b-151">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="a026b-151">-SslCertificateId</span></span>
<span data-ttu-id="a026b-152">Gibt die SSL-Zertifikat-ID (Secure Socket Layer) des HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="a026b-152">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="a026b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a026b-153">CommonParameters</span></span>
<span data-ttu-id="a026b-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a026b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a026b-155">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a026b-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a026b-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a026b-156">INPUTS</span></span>

### <span data-ttu-id="a026b-157">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a026b-157">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a026b-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a026b-158">OUTPUTS</span></span>

### <span data-ttu-id="a026b-159">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a026b-159">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a026b-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="a026b-160">NOTES</span></span>

## <span data-ttu-id="a026b-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a026b-161">RELATED LINKS</span></span>

[<span data-ttu-id="a026b-162">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a026b-162">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="a026b-163">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a026b-163">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="a026b-164">Neu – AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a026b-164">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="a026b-165">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a026b-165">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)


