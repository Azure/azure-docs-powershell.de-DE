---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1E192553-61D8-4449-936B-68CF866C710C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 571739c72b42e07070a3882ef696388a4a923196
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503578"
---
# <span data-ttu-id="5ca02-101">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5ca02-101">Add-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="5ca02-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5ca02-102">SYNOPSIS</span></span>
<span data-ttu-id="5ca02-103">Fügt einen HTTP-Listener zu einem Anwendungsgateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="5ca02-103">Adds an HTTP listener to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ca02-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ca02-104">SYNTAX</span></span>

### <span data-ttu-id="5ca02-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5ca02-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ca02-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="5ca02-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ca02-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5ca02-107">DESCRIPTION</span></span>
<span data-ttu-id="5ca02-108">Mit dem Cmdlet **Add-AzureRmApplicationGatewayHttpListener** wird ein HTTP-Listener zu einem Anwendungsgateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5ca02-108">The **Add-AzureRmApplicationGatewayHttpListener** cmdlet adds a HTTP listener to an application gateway.</span></span>

## <span data-ttu-id="5ca02-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5ca02-109">EXAMPLES</span></span>

### <span data-ttu-id="5ca02-110">Beispiel 1: Hinzufügen eines HTTP-Listeners</span><span class="sxs-lookup"><span data-stu-id="5ca02-110">Example 1: Add a HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Appgw = Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "listener01" -Protocol "Http" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01
```

<span data-ttu-id="5ca02-111">Der erste Befehl ruft das Anwendungsgateway ab und speichert es in der $AppGw-Variablen. Mit dem zweiten Befehl wird der HTTP-Listener dem Anwendungsgateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5ca02-111">The first command gets the application gateway and stores it in the $AppGw variable.The second command adds the HTTP listener to the application gateway.</span></span>

### <span data-ttu-id="5ca02-112">Beispiel 2: Hinzufügen eines HTTPS-Listener mit SSL</span><span class="sxs-lookup"><span data-stu-id="5ca02-112">Example 2: Add a HTTPS listener with SSL</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIP01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="5ca02-113">Der erste Befehl ruft das Anwendungsgateway ab und speichert es in der $AppGw-Variablen.</span><span class="sxs-lookup"><span data-stu-id="5ca02-113">The first command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="5ca02-114">Mit dem zweiten Befehl wird der Listener, der das HTTPS-Protokoll verwendet, zum Anwendungsgateway hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5ca02-114">The second command adds the listener, which uses the HTTPS protocol, to the application gateway.</span></span>

## <span data-ttu-id="5ca02-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ca02-115">PARAMETERS</span></span>

### <span data-ttu-id="5ca02-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ca02-116">-ApplicationGateway</span></span>
<span data-ttu-id="5ca02-117">Gibt das Anwendungsgateway an, dem dieses Cmdlet einen HTTP-Listener hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="5ca02-117">Specifies the application gateway to which this cmdlet adds an HTTP listener.</span></span>

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

### <span data-ttu-id="5ca02-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ca02-118">-DefaultProfile</span></span>
<span data-ttu-id="5ca02-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5ca02-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca02-120">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="5ca02-120">-FrontendIPConfiguration</span></span>
<span data-ttu-id="5ca02-121">Gibt das Front-End-IP-Ressourcenobjekt des Application Gateway an.</span><span class="sxs-lookup"><span data-stu-id="5ca02-121">Specifies the application gateway front-end IP resource object.</span></span>

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

### <span data-ttu-id="5ca02-122">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="5ca02-122">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="5ca02-123">Gibt die Front-End-IP-ID des Application Gateway an.</span><span class="sxs-lookup"><span data-stu-id="5ca02-123">Specifies the application gateway front-end IP ID.</span></span>

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

### <span data-ttu-id="5ca02-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="5ca02-124">-FrontendPort</span></span>
<span data-ttu-id="5ca02-125">Gibt das Front-End-Port Objekt des Application Gateway an.</span><span class="sxs-lookup"><span data-stu-id="5ca02-125">Specifies the application gateway front-end port object.</span></span>

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

### <span data-ttu-id="5ca02-126">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="5ca02-126">-FrontendPortId</span></span>
<span data-ttu-id="5ca02-127">Gibt die Front-End-Port-ID des Application Gateway an.</span><span class="sxs-lookup"><span data-stu-id="5ca02-127">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="5ca02-128">-Hostname</span><span class="sxs-lookup"><span data-stu-id="5ca02-128">-HostName</span></span>
<span data-ttu-id="5ca02-129">Gibt den Hostnamen an, dem dieses Cmdlet einen HTTP-Listener hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="5ca02-129">Specifies the host name that this cmdlet adds a HTTP listener to.</span></span>

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

### <span data-ttu-id="5ca02-130">-Name</span><span class="sxs-lookup"><span data-stu-id="5ca02-130">-Name</span></span>
<span data-ttu-id="5ca02-131">Gibt den Namen des Front-End-Ports an, den dieser Befehl hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="5ca02-131">Specifies the name of the front-end port that this command adds.</span></span>

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

### <span data-ttu-id="5ca02-132">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="5ca02-132">-Protocol</span></span>
<span data-ttu-id="5ca02-133">Gibt das Protokoll des HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="5ca02-133">Specifies the protocol of the HTTP listener.</span></span>
<span data-ttu-id="5ca02-134">Sowohl HTTP als auch HTTPS werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5ca02-134">Both HTTP and HTTPS are supported.</span></span>

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

### <span data-ttu-id="5ca02-135">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="5ca02-135">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="5ca02-136">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="5ca02-136">-SslCertificate</span></span>
<span data-ttu-id="5ca02-137">Gibt das SSL-Zertifikat des HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="5ca02-137">Specifies the SSL certificate of the HTTP listener.</span></span>
<span data-ttu-id="5ca02-138">Muss angegeben werden, wenn HTTPS als Listener-Protokoll ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="5ca02-138">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="5ca02-139">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="5ca02-139">-SslCertificateId</span></span>
<span data-ttu-id="5ca02-140">Gibt die SSL-Zertifikat-ID des HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="5ca02-140">Specifies the SSL certificate ID of the HTTP listener.</span></span>
<span data-ttu-id="5ca02-141">Muss angegeben werden, wenn HTTPS als Listener-Protokoll ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="5ca02-141">Must be specified if HTTPS is chosen as listener protocol.</span></span>

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

### <span data-ttu-id="5ca02-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ca02-142">CommonParameters</span></span>
<span data-ttu-id="5ca02-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ca02-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ca02-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ca02-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ca02-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5ca02-145">INPUTS</span></span>

### <span data-ttu-id="5ca02-146">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ca02-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="5ca02-147">Parameter: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5ca02-147">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="5ca02-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5ca02-148">OUTPUTS</span></span>

### <span data-ttu-id="5ca02-149">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ca02-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5ca02-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="5ca02-150">NOTES</span></span>

## <span data-ttu-id="5ca02-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5ca02-151">RELATED LINKS</span></span>

[<span data-ttu-id="5ca02-152">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5ca02-152">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="5ca02-153">Neu – AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5ca02-153">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="5ca02-154">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5ca02-154">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="5ca02-155">Satz-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="5ca02-155">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


