---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 11a416e237ff4a12dc3aafbd161e1ae77faab732
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822779"
---
# <span data-ttu-id="85c59-101">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="85c59-101">Set-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="85c59-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="85c59-102">SYNOPSIS</span></span>
<span data-ttu-id="85c59-103">Ändert einen HTTP-Listener für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="85c59-103">Modifies an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="85c59-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="85c59-104">SYNTAX</span></span>

### <span data-ttu-id="85c59-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="85c59-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="85c59-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="85c59-106">SetByResource</span></span>
```
Set-AzApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="85c59-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="85c59-107">DESCRIPTION</span></span>
<span data-ttu-id="85c59-108">Das Cmdlet " **Satz-AzApplicationGatewayHttpListener** " ändert einen HTTP-Listener für ein Azure Application-Gateway.</span><span class="sxs-lookup"><span data-stu-id="85c59-108">The **Set-AzApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="85c59-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="85c59-109">EXAMPLES</span></span>

### <span data-ttu-id="85c59-110">Beispiel 1: Einrichten eines HTTP-Listener</span><span class="sxs-lookup"><span data-stu-id="85c59-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="85c59-111">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="85c59-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="85c59-112">Der zweite Befehl legt den HTTP-Listener für das Gateway so fest, dass die in $FIP 01 gespeicherte Front-End-Konfiguration mit dem HTTP-Protokoll auf Port 80 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="85c59-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

## <span data-ttu-id="85c59-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="85c59-113">PARAMETERS</span></span>

### <span data-ttu-id="85c59-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="85c59-114">-ApplicationGateway</span></span>
<span data-ttu-id="85c59-115">Gibt das Anwendungsgateway an, mit dem dieses Cmdlet den HTTP-Listener verknüpft.</span><span class="sxs-lookup"><span data-stu-id="85c59-115">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="85c59-116">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="85c59-116">-CustomErrorConfiguration</span></span>
<span data-ttu-id="85c59-117">Kunden Fehler eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="85c59-117">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="85c59-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85c59-118">-DefaultProfile</span></span>
<span data-ttu-id="85c59-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="85c59-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85c59-120">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="85c59-120">-FrontendIPConfiguration</span></span>
<span data-ttu-id="85c59-121">Gibt die Front-End-IP-Adresse des Anwendungs Gateways an.</span><span class="sxs-lookup"><span data-stu-id="85c59-121">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="85c59-122">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="85c59-122">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="85c59-123">Gibt die ID der Front-End-IP-Adresse des Anwendungs Gateways an.</span><span class="sxs-lookup"><span data-stu-id="85c59-123">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="85c59-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="85c59-124">-FrontendPort</span></span>
<span data-ttu-id="85c59-125">Gibt den Front-End-Port des Application Gateway an.</span><span class="sxs-lookup"><span data-stu-id="85c59-125">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="85c59-126">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="85c59-126">-FrontendPortId</span></span>
<span data-ttu-id="85c59-127">Gibt die Front-End-Port-ID des Application Gateway an.</span><span class="sxs-lookup"><span data-stu-id="85c59-127">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="85c59-128">-Hostname</span><span class="sxs-lookup"><span data-stu-id="85c59-128">-HostName</span></span>
<span data-ttu-id="85c59-129">Gibt den Hostnamen an, an den dieses Cmdlet den HTTP-Listener sendet.</span><span class="sxs-lookup"><span data-stu-id="85c59-129">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="85c59-130">-Name</span><span class="sxs-lookup"><span data-stu-id="85c59-130">-Name</span></span>
<span data-ttu-id="85c59-131">Gibt den Namen des HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="85c59-131">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="85c59-132">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="85c59-132">-Protocol</span></span>
<span data-ttu-id="85c59-133">Gibt das Protokoll an, das der HTTP-Listener verwendet.</span><span class="sxs-lookup"><span data-stu-id="85c59-133">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="85c59-134">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="85c59-134">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="85c59-135">Http</span><span class="sxs-lookup"><span data-stu-id="85c59-135">Http</span></span>
- <span data-ttu-id="85c59-136">HTTPS</span><span class="sxs-lookup"><span data-stu-id="85c59-136">Https</span></span>

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

### <span data-ttu-id="85c59-137">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="85c59-137">-RequireServerNameIndication</span></span>
<span data-ttu-id="85c59-138">Gibt an, ob für das Cmdlet eine Servernamen Angabe erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="85c59-138">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="85c59-139">Die zulässigen Werte für diesen Parameter lauten: wahr oder falsch.</span><span class="sxs-lookup"><span data-stu-id="85c59-139">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="85c59-140">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="85c59-140">-SslCertificate</span></span>
<span data-ttu-id="85c59-141">Gibt das SSL-Zertifikat des HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="85c59-141">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="85c59-142">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="85c59-142">-SslCertificateId</span></span>
<span data-ttu-id="85c59-143">Gibt die SSL-Zertifikat-ID (Secure Socket Layer) des HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="85c59-143">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="85c59-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85c59-144">CommonParameters</span></span>
<span data-ttu-id="85c59-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85c59-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85c59-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85c59-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85c59-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="85c59-147">INPUTS</span></span>

### <span data-ttu-id="85c59-148">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="85c59-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="85c59-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="85c59-149">OUTPUTS</span></span>

### <span data-ttu-id="85c59-150">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="85c59-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="85c59-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="85c59-151">NOTES</span></span>

## <span data-ttu-id="85c59-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="85c59-152">RELATED LINKS</span></span>

[<span data-ttu-id="85c59-153">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="85c59-153">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="85c59-154">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="85c59-154">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="85c59-155">Neu – AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="85c59-155">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="85c59-156">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="85c59-156">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)


