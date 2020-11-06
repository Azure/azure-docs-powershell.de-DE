---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 231ee3dc8d66d3960f0416cb410b6747b25ae278
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503466"
---
# <span data-ttu-id="77293-101">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="77293-101">Set-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="77293-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="77293-102">SYNOPSIS</span></span>
<span data-ttu-id="77293-103">Ändert einen HTTP-Listener für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="77293-103">Modifies an HTTP listener for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77293-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="77293-104">SYNTAX</span></span>

### <span data-ttu-id="77293-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="77293-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77293-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="77293-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77293-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="77293-107">DESCRIPTION</span></span>
<span data-ttu-id="77293-108">Das Cmdlet " **Satz-AzureRmApplicationGatewayHttpListener** " ändert einen HTTP-Listener für ein Azure Application-Gateway.</span><span class="sxs-lookup"><span data-stu-id="77293-108">The **Set-AzureRmApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="77293-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="77293-109">EXAMPLES</span></span>

### <span data-ttu-id="77293-110">Beispiel 1: Einrichten eines HTTP-Listener</span><span class="sxs-lookup"><span data-stu-id="77293-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="77293-111">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="77293-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="77293-112">Der zweite Befehl legt den HTTP-Listener für das Gateway so fest, dass die in $FIP 01 gespeicherte Front-End-Konfiguration mit dem HTTP-Protokoll auf Port 80 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="77293-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

## <span data-ttu-id="77293-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="77293-113">PARAMETERS</span></span>

### <span data-ttu-id="77293-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="77293-114">-ApplicationGateway</span></span>
<span data-ttu-id="77293-115">Gibt das Anwendungsgateway an, mit dem dieses Cmdlet den HTTP-Listener verknüpft.</span><span class="sxs-lookup"><span data-stu-id="77293-115">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

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

### <span data-ttu-id="77293-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77293-116">-DefaultProfile</span></span>
<span data-ttu-id="77293-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="77293-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77293-118">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="77293-118">-FrontendIPConfiguration</span></span>
<span data-ttu-id="77293-119">Gibt die Front-End-IP-Adresse des Anwendungs Gateways an.</span><span class="sxs-lookup"><span data-stu-id="77293-119">Specifies the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="77293-120">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="77293-120">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="77293-121">Gibt die ID der Front-End-IP-Adresse des Anwendungs Gateways an.</span><span class="sxs-lookup"><span data-stu-id="77293-121">Specifies the ID of the front-end IP address of the application gateway.</span></span>

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

### <span data-ttu-id="77293-122">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="77293-122">-FrontendPort</span></span>
<span data-ttu-id="77293-123">Gibt den Front-End-Port des Application Gateway an.</span><span class="sxs-lookup"><span data-stu-id="77293-123">Specifies the application gateway front-end port.</span></span>

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

### <span data-ttu-id="77293-124">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="77293-124">-FrontendPortId</span></span>
<span data-ttu-id="77293-125">Gibt die Front-End-Port-ID des Application Gateway an.</span><span class="sxs-lookup"><span data-stu-id="77293-125">Specifies the application gateway front-end port ID.</span></span>

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

### <span data-ttu-id="77293-126">-Hostname</span><span class="sxs-lookup"><span data-stu-id="77293-126">-HostName</span></span>
<span data-ttu-id="77293-127">Gibt den Hostnamen an, an den dieses Cmdlet den HTTP-Listener sendet.</span><span class="sxs-lookup"><span data-stu-id="77293-127">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

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

### <span data-ttu-id="77293-128">-Name</span><span class="sxs-lookup"><span data-stu-id="77293-128">-Name</span></span>
<span data-ttu-id="77293-129">Gibt den Namen des HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="77293-129">Specifies the name of the HTTP listener.</span></span>

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

### <span data-ttu-id="77293-130">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="77293-130">-Protocol</span></span>
<span data-ttu-id="77293-131">Gibt das Protokoll an, das der HTTP-Listener verwendet.</span><span class="sxs-lookup"><span data-stu-id="77293-131">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="77293-132">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="77293-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="77293-133">Http</span><span class="sxs-lookup"><span data-stu-id="77293-133">Http</span></span>
- <span data-ttu-id="77293-134">HTTPS</span><span class="sxs-lookup"><span data-stu-id="77293-134">Https</span></span>

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

### <span data-ttu-id="77293-135">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="77293-135">-RequireServerNameIndication</span></span>
<span data-ttu-id="77293-136">Gibt an, ob für das Cmdlet eine Servernamen Angabe erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="77293-136">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="77293-137">Die zulässigen Werte für diesen Parameter lauten: wahr oder falsch.</span><span class="sxs-lookup"><span data-stu-id="77293-137">The acceptable values for this parameter are: true or false.</span></span>

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

### <span data-ttu-id="77293-138">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="77293-138">-SslCertificate</span></span>
<span data-ttu-id="77293-139">Gibt das SSL-Zertifikat des HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="77293-139">Specifies the SSL certificate of the HTTP listener.</span></span>

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

### <span data-ttu-id="77293-140">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="77293-140">-SslCertificateId</span></span>
<span data-ttu-id="77293-141">Gibt die SSL-Zertifikat-ID (Secure Socket Layer) des HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="77293-141">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

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

### <span data-ttu-id="77293-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77293-142">CommonParameters</span></span>
<span data-ttu-id="77293-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77293-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77293-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77293-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77293-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="77293-145">INPUTS</span></span>

### <span data-ttu-id="77293-146">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="77293-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="77293-147">Parameter: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="77293-147">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="77293-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="77293-148">OUTPUTS</span></span>

### <span data-ttu-id="77293-149">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="77293-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="77293-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="77293-150">NOTES</span></span>

## <span data-ttu-id="77293-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="77293-151">RELATED LINKS</span></span>

[<span data-ttu-id="77293-152">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="77293-152">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="77293-153">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="77293-153">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="77293-154">Neu – AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="77293-154">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="77293-155">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="77293-155">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)


