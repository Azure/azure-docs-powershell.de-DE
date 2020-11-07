---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayhttplistener
schema: 2.0.0
ms.openlocfilehash: f6b8e2a869ba6c59011241c5ebb7b1fe46ac2bc7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848436"
---
# <span data-ttu-id="a91c3-101">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a91c3-101">New-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="a91c3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a91c3-102">SYNOPSIS</span></span>
<span data-ttu-id="a91c3-103">Erstellt einen HTTP-Listener für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="a91c3-103">Creates an HTTP listener for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a91c3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a91c3-104">SYNTAX</span></span>

### <span data-ttu-id="a91c3-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a91c3-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-HostName <String>]
 [-RequireServerNameIndication <String>] -Protocol <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a91c3-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="a91c3-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a91c3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a91c3-107">DESCRIPTION</span></span>
<span data-ttu-id="a91c3-108">Das Cmdlet **New-AzureRmApplicationGatewayHttpListener** erstellt einen HTTP-Listener für ein Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="a91c3-108">The **New-AzureRmApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="a91c3-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a91c3-109">EXAMPLES</span></span>

### <span data-ttu-id="a91c3-110">Beispiel 1: Erstellen eines HTTP-Listeners</span><span class="sxs-lookup"><span data-stu-id="a91c3-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzureRmApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="a91c3-111">Dieser Befehl erstellt einen HTTP-Listener mit dem Namen Listener01 und speichert das Ergebnis in der Variablen mit dem Namen $Listener.</span><span class="sxs-lookup"><span data-stu-id="a91c3-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="a91c3-112">Beispiel 2: Erstellen eines HTTP-Listener mit SSL</span><span class="sxs-lookup"><span data-stu-id="a91c3-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzureRmApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="a91c3-113">Dieser Befehl erstellt einen HTTP-Listener, der SSL-Entlastung verwendet und das SSL-Zertifikat in der $SSLCert 01-Variable bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="a91c3-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="a91c3-114">Der Befehl speichert das Ergebnis in der Variablen mit dem Namen $Listener.</span><span class="sxs-lookup"><span data-stu-id="a91c3-114">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="a91c3-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="a91c3-115">PARAMETERS</span></span>

### <span data-ttu-id="a91c3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a91c3-116">-DefaultProfile</span></span>
<span data-ttu-id="a91c3-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a91c3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a91c3-118">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a91c3-118">-FrontendIPConfiguration</span></span>
<span data-ttu-id="a91c3-119">Gibt das Front-End-IP-Konfigurationsobjekt für den HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="a91c3-119">Specifies front-end IP configuration object for the HTTP listener.</span></span>

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

### <span data-ttu-id="a91c3-120">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="a91c3-120">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="a91c3-121">Gibt die ID der Front-End-IP-Konfiguration für den HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="a91c3-121">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="a91c3-122">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="a91c3-122">-FrontendPort</span></span>
<span data-ttu-id="a91c3-123">Gibt den Front-End-Port für den HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="a91c3-123">Specifies the front-end port for the HTTP listener.</span></span>

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

### <span data-ttu-id="a91c3-124">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="a91c3-124">-FrontendPortId</span></span>
<span data-ttu-id="a91c3-125">Gibt die ID des Front-End-Port Objekts für den HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="a91c3-125">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="a91c3-126">-Hostname</span><span class="sxs-lookup"><span data-stu-id="a91c3-126">-HostName</span></span>
<span data-ttu-id="a91c3-127">Gibt den Hostnamen des Application Gateway HTTP-Listeners an.</span><span class="sxs-lookup"><span data-stu-id="a91c3-127">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="a91c3-128">-Name</span><span class="sxs-lookup"><span data-stu-id="a91c3-128">-Name</span></span>
<span data-ttu-id="a91c3-129">Gibt den Namen des vom Cmdlet erstellten HTTP-Listeners an.</span><span class="sxs-lookup"><span data-stu-id="a91c3-129">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="a91c3-130">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="a91c3-130">-Protocol</span></span>
<span data-ttu-id="a91c3-131">Gibt das Protokoll an, das der HTTP-Listener verwendet.</span><span class="sxs-lookup"><span data-stu-id="a91c3-131">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="a91c3-132">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="a91c3-132">-RequireServerNameIndication</span></span>
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

### <span data-ttu-id="a91c3-133">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="a91c3-133">-SslCertificate</span></span>
<span data-ttu-id="a91c3-134">Gibt das SSL-Zertifikatobjekt für den HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="a91c3-134">Specifies the SSL certificate object for  the HTTP listener.</span></span>

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

### <span data-ttu-id="a91c3-135">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="a91c3-135">-SslCertificateId</span></span>
<span data-ttu-id="a91c3-136">Gibt die ID des SSL-Zertifikats für den HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="a91c3-136">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="a91c3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a91c3-137">CommonParameters</span></span>
<span data-ttu-id="a91c3-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a91c3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a91c3-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a91c3-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a91c3-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a91c3-140">INPUTS</span></span>

### <span data-ttu-id="a91c3-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a91c3-141">System.String</span></span>

## <span data-ttu-id="a91c3-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a91c3-142">OUTPUTS</span></span>

### <span data-ttu-id="a91c3-143">Microsoft. Azure. Commands. Network. Models. PSHttpListener</span><span class="sxs-lookup"><span data-stu-id="a91c3-143">Microsoft.Azure.Commands.Network.Models.PSHttpListener</span></span>

## <span data-ttu-id="a91c3-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="a91c3-144">NOTES</span></span>

## <span data-ttu-id="a91c3-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a91c3-145">RELATED LINKS</span></span>

[<span data-ttu-id="a91c3-146">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a91c3-146">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="a91c3-147">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a91c3-147">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="a91c3-148">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a91c3-148">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="a91c3-149">Satz-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="a91c3-149">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


