---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 5648bb1cb7497517afb5ff461674294e426c0131
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660951"
---
# <span data-ttu-id="de121-101">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="de121-101">Add-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="de121-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="de121-102">SYNOPSIS</span></span>
<span data-ttu-id="de121-103">Fügt einen HTTP-Listener zu einem Anwendungsgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="de121-103">Adds an HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="de121-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="de121-104">SYNTAX</span></span>

### <span data-ttu-id="de121-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="de121-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="de121-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="de121-106">SetByResource</span></span>
```
Add-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="de121-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="de121-107">DESCRIPTION</span></span>
<span data-ttu-id="de121-108">Mit dem Cmdlet **Add-AzApplicationGatewayHttpListener** wird ein HTTP-Listener zu einem Anwendungsgateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="de121-108">The **Add-AzApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="de121-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="de121-109">EXAMPLES</span></span>

### <span data-ttu-id="de121-110">Beispiel 1: Hinzufügen eines HTTP-Listeners</span><span class="sxs-lookup"><span data-stu-id="de121-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="de121-111">Der erste Befehl ruft das Anwendungsgateway ab und speichert es in der $AppGw-Variablen. Mit dem zweiten Befehl wird der HTTP-Listener dem Anwendungsgateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="de121-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="de121-112">Beispiel 2: Hinzufügen eines HTTPS-Listener mit SSL</span><span class="sxs-lookup"><span data-stu-id="de121-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="de121-113">Der erste Befehl ruft das Anwendungsgateway ab und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="de121-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="de121-114">Mit dem zweiten Befehl wird der Listener, der das HTTPS-Protokoll verwendet, zum Anwendungsgateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="de121-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

## <span data-ttu-id="de121-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="de121-115">PARAMETERS</span></span>

### <span data-ttu-id="de121-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="de121-116">-ApplicationGateway</span></span>
<span data-ttu-id="de121-117">Gibt das Anwendungsgateway an, dem dieses Cmdlet einen HTTP-Listener hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="de121-117">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

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

### <span data-ttu-id="de121-118">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="de121-118">-CustomErrorConfiguration</span></span>
<span data-ttu-id="de121-119">Kunden Fehler eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="de121-119">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="de121-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de121-120">-DefaultProfile</span></span>
<span data-ttu-id="de121-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="de121-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de121-122">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="de121-122">-FrontendIPConfiguration</span></span>
<span data-ttu-id="de121-123">Gibt das Front-End-IP-Ressourcenobjekt des Application Gateway an.</span><span class="sxs-lookup"><span data-stu-id="de121-123">Specifies the application gateway front-end IP resource object.</span></span>

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

### <span data-ttu-id="de121-124">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="de121-124">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="de121-125">Gibt die Front-End-IP-ID des Application Gateway an.</span><span class="sxs-lookup"><span data-stu-id="de121-125">Specifies the application gateway front-end IP ID.</span></span>

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

### <span data-ttu-id="de121-126">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="de121-126">-FrontendPort</span></span>
<span data-ttu-id="de121-127">Gibt das Front-End-Port Objekt des Application Gateway an.</span><span class="sxs-lookup"><span data-stu-id="de121-127">Specifies the application gateway front-end port object.</span></span>

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

### <span data-ttu-id="de121-128">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="de121-128">-FrontendPortId</span></span>
<span data-ttu-id="de121-129">Gibt die Front-End-Port-ID des Application Gateway an.</span><span class="sxs-lookup"><span data-stu-id="de121-129">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="de121-130">-Hostname</span><span class="sxs-lookup"><span data-stu-id="de121-130">-HostName</span></span>
<span data-ttu-id="de121-131">Gibt den Hostnamen an, dem dieses Cmdlet einen HTTP-Listener hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="de121-131">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

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

### <span data-ttu-id="de121-132">-Name</span><span class="sxs-lookup"><span data-stu-id="de121-132">-Name</span></span>
<span data-ttu-id="de121-133">Gibt den Namen des Front-End-Ports an, den dieser Befehl hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="de121-133">Specifies the name of the front-end port that this command adds.</span></span>

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

### <span data-ttu-id="de121-134">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="de121-134">-Protocol</span></span>
<span data-ttu-id="de121-135">Gibt das Protokoll des HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="de121-135">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="de121-136">Sowohl HTTP als auch HTTPS werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="de121-136">Both HTTP and HTTPS are supported.</span></span>

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

### <span data-ttu-id="de121-137">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="de121-137">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="de121-138">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="de121-138">-SslCertificate</span></span>
<span data-ttu-id="de121-139">Gibt das SSL-Zertifikat des HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="de121-139">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="de121-140">Muss angegeben werden, wenn HTTPS als Listener-Protokoll ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="de121-140">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="de121-141">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="de121-141">-SslCertificateId</span></span>
<span data-ttu-id="de121-142">Gibt die SSL-Zertifikat-ID des HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="de121-142">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="de121-143">Muss angegeben werden, wenn HTTPS als Listener-Protokoll ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="de121-143">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="de121-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de121-144">CommonParameters</span></span>
<span data-ttu-id="de121-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de121-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de121-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de121-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de121-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="de121-147">INPUTS</span></span>

### <span data-ttu-id="de121-148">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="de121-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="de121-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="de121-149">OUTPUTS</span></span>

### <span data-ttu-id="de121-150">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="de121-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="de121-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="de121-151">NOTES</span></span>

## <span data-ttu-id="de121-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="de121-152">RELATED LINKS</span></span>

[<span data-ttu-id="de121-153">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="de121-153">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="de121-154">Neu – AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="de121-154">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="de121-155">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="de121-155">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="de121-156">Satz-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="de121-156">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


