---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8068AF1-3380-4E60-B6CF-CC584BD053A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayhttplistener
schema: 2.0.0
ms.openlocfilehash: 7b3d38b8f55c93c4527d92969ec64ce792bca44b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848120"
---
# <span data-ttu-id="77a72-101">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="77a72-101">Set-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="77a72-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="77a72-102">SYNOPSIS</span></span>
<span data-ttu-id="77a72-103">Ändert einen HTTP-Listener für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="77a72-103">Modifies an HTTP listener for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77a72-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="77a72-104">SYNTAX</span></span>

### <span data-ttu-id="77a72-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="77a72-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfigurationId <String>] [-FrontendPortId <String>] [-SslCertificateId <String>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77a72-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="77a72-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77a72-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="77a72-107">DESCRIPTION</span></span>
<span data-ttu-id="77a72-108">Das Cmdlet " **Satz-AzureRmApplicationGatewayHttpListener** " ändert einen HTTP-Listener für ein Azure Application-Gateway.</span><span class="sxs-lookup"><span data-stu-id="77a72-108">The **Set-AzureRmApplicationGatewayHttpListener** cmdlet modifies an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="77a72-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="77a72-109">EXAMPLES</span></span>

### <span data-ttu-id="77a72-110">Beispiel 1: Einrichten eines HTTP-Listener</span><span class="sxs-lookup"><span data-stu-id="77a72-110">Example 1: Set an HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener01" -Protocol Http -FrontendIpConfiguration $FIP01 -FrontendPort 80
```

<span data-ttu-id="77a72-111">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="77a72-111">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="77a72-112">Der zweite Befehl legt den HTTP-Listener für das Gateway so fest, dass die in $FIP 01 gespeicherte Front-End-Konfiguration mit dem HTTP-Protokoll auf Port 80 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="77a72-112">The second command sets the HTTP listener for the gateway to use the front-end configuration stored in $FIP01 with the HTTP protocol on port 80.</span></span>

## <span data-ttu-id="77a72-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="77a72-113">PARAMETERS</span></span>

### <span data-ttu-id="77a72-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="77a72-114">-ApplicationGateway</span></span>
<span data-ttu-id="77a72-115">Gibt das Anwendungsgateway an, mit dem dieses Cmdlet den HTTP-Listener verknüpft.</span><span class="sxs-lookup"><span data-stu-id="77a72-115">Specifies the application gateway with which this cmdlet associates the HTTP listener.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77a72-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77a72-116">-DefaultProfile</span></span>
<span data-ttu-id="77a72-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="77a72-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77a72-118">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="77a72-118">-FrontendIPConfiguration</span></span>
<span data-ttu-id="77a72-119">Gibt die Front-End-IP-Adresse des Anwendungs Gateways an.</span><span class="sxs-lookup"><span data-stu-id="77a72-119">Specifies the front-end IP address of the application gateway.</span></span>

```yaml
Type: PSApplicationGatewayFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77a72-120">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="77a72-120">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="77a72-121">Gibt die ID der Front-End-IP-Adresse des Anwendungs Gateways an.</span><span class="sxs-lookup"><span data-stu-id="77a72-121">Specifies the ID of the front-end IP address of the application gateway.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77a72-122">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="77a72-122">-FrontendPort</span></span>
<span data-ttu-id="77a72-123">Gibt den Front-End-Port des Application Gateway an.</span><span class="sxs-lookup"><span data-stu-id="77a72-123">Specifies the application gateway front-end port.</span></span>

```yaml
Type: PSApplicationGatewayFrontendPort
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77a72-124">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="77a72-124">-FrontendPortId</span></span>
<span data-ttu-id="77a72-125">Gibt die Front-End-Port-ID des Application Gateway an.</span><span class="sxs-lookup"><span data-stu-id="77a72-125">Specifies the application gateway front-end port ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77a72-126">-Hostname</span><span class="sxs-lookup"><span data-stu-id="77a72-126">-HostName</span></span>
<span data-ttu-id="77a72-127">Gibt den Hostnamen an, an den dieses Cmdlet den HTTP-Listener sendet.</span><span class="sxs-lookup"><span data-stu-id="77a72-127">Specifies the host name that this cmdlet sends the HTTP listener to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77a72-128">-Name</span><span class="sxs-lookup"><span data-stu-id="77a72-128">-Name</span></span>
<span data-ttu-id="77a72-129">Gibt den Namen des HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="77a72-129">Specifies the name of the HTTP listener.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77a72-130">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="77a72-130">-Protocol</span></span>
<span data-ttu-id="77a72-131">Gibt das Protokoll an, das der HTTP-Listener verwendet.</span><span class="sxs-lookup"><span data-stu-id="77a72-131">Specifies the protocol that the HTTP listener uses.</span></span>
<span data-ttu-id="77a72-132">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="77a72-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="77a72-133">Http</span><span class="sxs-lookup"><span data-stu-id="77a72-133">Http</span></span>
- <span data-ttu-id="77a72-134">HTTPS</span><span class="sxs-lookup"><span data-stu-id="77a72-134">Https</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77a72-135">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="77a72-135">-RequireServerNameIndication</span></span>
<span data-ttu-id="77a72-136">Gibt an, ob für das Cmdlet eine Servernamen Angabe erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="77a72-136">Specifies whether the cmdlet requires a server name indication.</span></span>
<span data-ttu-id="77a72-137">Die zulässigen Werte für diesen Parameter lauten: wahr oder falsch.</span><span class="sxs-lookup"><span data-stu-id="77a72-137">The acceptable values for this parameter are: true or false.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: true, false

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77a72-138">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="77a72-138">-SslCertificate</span></span>
<span data-ttu-id="77a72-139">Gibt das SSL-Zertifikat des HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="77a72-139">Specifies the SSL certificate of the HTTP listener.</span></span>

```yaml
Type: PSApplicationGatewaySslCertificate
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77a72-140">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="77a72-140">-SslCertificateId</span></span>
<span data-ttu-id="77a72-141">Gibt die SSL-Zertifikat-ID (Secure Socket Layer) des HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="77a72-141">Specifies the Secure Socket Layer (SSL) certificate ID of the HTTP listener.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77a72-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77a72-142">CommonParameters</span></span>
<span data-ttu-id="77a72-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77a72-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77a72-144">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77a72-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77a72-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="77a72-145">INPUTS</span></span>

### <span data-ttu-id="77a72-146">System. String</span><span class="sxs-lookup"><span data-stu-id="77a72-146">System.String</span></span>

## <span data-ttu-id="77a72-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="77a72-147">OUTPUTS</span></span>

### <span data-ttu-id="77a72-148">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="77a72-148">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="77a72-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="77a72-149">NOTES</span></span>

## <span data-ttu-id="77a72-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="77a72-150">RELATED LINKS</span></span>

[<span data-ttu-id="77a72-151">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="77a72-151">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="77a72-152">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="77a72-152">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="77a72-153">Neu – AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="77a72-153">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="77a72-154">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="77a72-154">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)


