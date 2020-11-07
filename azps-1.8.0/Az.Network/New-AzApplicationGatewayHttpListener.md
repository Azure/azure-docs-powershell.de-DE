---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AF8CC409-2EA7-4EC1-86C9-E7A773DE9201
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: e5593ae97692813cc36f14942edb21768517f317
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660613"
---
# <span data-ttu-id="13d5b-101">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="13d5b-101">New-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="13d5b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="13d5b-102">SYNOPSIS</span></span>
<span data-ttu-id="13d5b-103">Erstellt einen HTTP-Listener für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="13d5b-103">Creates an HTTP listener for an application gateway.</span></span>

## <span data-ttu-id="13d5b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="13d5b-104">SYNTAX</span></span>

### <span data-ttu-id="13d5b-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="13d5b-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String> [-FrontendIPConfigurationId <String>]
 [-FrontendPortId <String>] [-SslCertificateId <String>] [-HostName <String>]
 [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="13d5b-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="13d5b-106">SetByResource</span></span>
```
New-AzApplicationGatewayHttpListener -Name <String>
 [-FrontendIPConfiguration <PSApplicationGatewayFrontendIPConfiguration>]
 [-FrontendPort <PSApplicationGatewayFrontendPort>] [-SslCertificate <PSApplicationGatewaySslCertificate>]
 [-HostName <String>] [-RequireServerNameIndication <String>] -Protocol <String>
 [-CustomErrorConfiguration <PSApplicationGatewayCustomError[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="13d5b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="13d5b-107">DESCRIPTION</span></span>
<span data-ttu-id="13d5b-108">Das Cmdlet **New-AzApplicationGatewayHttpListener** erstellt einen HTTP-Listener für ein Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="13d5b-108">The **New-AzApplicationGatewayHttpListener** cmdlet creates an HTTP listener for an Azure application gateway.</span></span>

## <span data-ttu-id="13d5b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="13d5b-109">EXAMPLES</span></span>

### <span data-ttu-id="13d5b-110">Beispiel 1: Erstellen eines HTTP-Listeners</span><span class="sxs-lookup"><span data-stu-id="13d5b-110">Example 1: Create an HTTP listener</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Http" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01
```

<span data-ttu-id="13d5b-111">Dieser Befehl erstellt einen HTTP-Listener mit dem Namen Listener01 und speichert das Ergebnis in der Variablen mit dem Namen $Listener.</span><span class="sxs-lookup"><span data-stu-id="13d5b-111">This command creates an HTTP listener named Listener01 and stores the result in the variable named $Listener.</span></span>

### <span data-ttu-id="13d5b-112">Beispiel 2: Erstellen eines HTTP-Listener mit SSL</span><span class="sxs-lookup"><span data-stu-id="13d5b-112">Example 2: Create an HTTP listener with SSL</span></span>
```
PS C:\>$Listener = New-AzApplicationGatewayHttpListener -Name "Listener01" -Protocol "Https" -FrontendIpConfiguration $FIp01 -FrontendPort $FP01 -SslCertificate $SSLCert01
```

<span data-ttu-id="13d5b-113">Dieser Befehl erstellt einen HTTP-Listener, der SSL-Entlastung verwendet und das SSL-Zertifikat in der $SSLCert 01-Variable bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="13d5b-113">This command creates an HTTP listener that uses SSL offload and provides the SSL certificate in the $SSLCert01 variable.</span></span>
<span data-ttu-id="13d5b-114">Der Befehl speichert das Ergebnis in der Variablen mit dem Namen $Listener.</span><span class="sxs-lookup"><span data-stu-id="13d5b-114">The command stores the result in the variable named $Listener.</span></span>

## <span data-ttu-id="13d5b-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="13d5b-115">PARAMETERS</span></span>

### <span data-ttu-id="13d5b-116">-CustomErrorConfiguration</span><span class="sxs-lookup"><span data-stu-id="13d5b-116">-CustomErrorConfiguration</span></span>
<span data-ttu-id="13d5b-117">Kunden Fehler eines Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="13d5b-117">Customer error of an application gateway</span></span>

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

### <span data-ttu-id="13d5b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13d5b-118">-DefaultProfile</span></span>
<span data-ttu-id="13d5b-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="13d5b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13d5b-120">-FrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="13d5b-120">-FrontendIPConfiguration</span></span>
<span data-ttu-id="13d5b-121">Gibt das Front-End-IP-Konfigurationsobjekt für den HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="13d5b-121">Specifies front-end IP configuration object for the HTTP listener.</span></span>

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

### <span data-ttu-id="13d5b-122">-FrontendIPConfigurationId</span><span class="sxs-lookup"><span data-stu-id="13d5b-122">-FrontendIPConfigurationId</span></span>
<span data-ttu-id="13d5b-123">Gibt die ID der Front-End-IP-Konfiguration für den HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="13d5b-123">Specifies the ID of the front-end IP configuration for the HTTP listener.</span></span>

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

### <span data-ttu-id="13d5b-124">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="13d5b-124">-FrontendPort</span></span>
<span data-ttu-id="13d5b-125">Gibt den Front-End-Port für den HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="13d5b-125">Specifies the front-end port for the HTTP listener.</span></span>

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

### <span data-ttu-id="13d5b-126">-FrontendPortId</span><span class="sxs-lookup"><span data-stu-id="13d5b-126">-FrontendPortId</span></span>
<span data-ttu-id="13d5b-127">Gibt die ID des Front-End-Port Objekts für den HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="13d5b-127">Specifies the ID of the front-end port object for the HTTP listener.</span></span>

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

### <span data-ttu-id="13d5b-128">-Hostname</span><span class="sxs-lookup"><span data-stu-id="13d5b-128">-HostName</span></span>
<span data-ttu-id="13d5b-129">Gibt den Hostnamen des Application Gateway HTTP-Listeners an.</span><span class="sxs-lookup"><span data-stu-id="13d5b-129">Specifies the host name of the application gateway HTTP listener.</span></span>

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

### <span data-ttu-id="13d5b-130">-Name</span><span class="sxs-lookup"><span data-stu-id="13d5b-130">-Name</span></span>
<span data-ttu-id="13d5b-131">Gibt den Namen des vom Cmdlet erstellten HTTP-Listeners an.</span><span class="sxs-lookup"><span data-stu-id="13d5b-131">Specifies the name of the HTTP listener that this cmdlet creates.</span></span>

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

### <span data-ttu-id="13d5b-132">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="13d5b-132">-Protocol</span></span>
<span data-ttu-id="13d5b-133">Gibt das Protokoll an, das der HTTP-Listener verwendet.</span><span class="sxs-lookup"><span data-stu-id="13d5b-133">Specifies the protocol that the HTTP listener uses.</span></span>

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

### <span data-ttu-id="13d5b-134">-RequireServerNameIndication</span><span class="sxs-lookup"><span data-stu-id="13d5b-134">-RequireServerNameIndication</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: true, false

Required: False
Position: Named
Default value: true
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13d5b-135">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="13d5b-135">-SslCertificate</span></span>
<span data-ttu-id="13d5b-136">Gibt das SSL-Zertifikatobjekt für den HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="13d5b-136">Specifies the SSL certificate object for the HTTP listener.</span></span>

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

### <span data-ttu-id="13d5b-137">-SslCertificateId</span><span class="sxs-lookup"><span data-stu-id="13d5b-137">-SslCertificateId</span></span>
<span data-ttu-id="13d5b-138">Gibt die ID des SSL-Zertifikats für den HTTP-Listener an.</span><span class="sxs-lookup"><span data-stu-id="13d5b-138">Specifies the ID of the SSL certificate for the HTTP listener.</span></span>

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

### <span data-ttu-id="13d5b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13d5b-139">CommonParameters</span></span>
<span data-ttu-id="13d5b-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13d5b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13d5b-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13d5b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13d5b-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="13d5b-142">INPUTS</span></span>

### <span data-ttu-id="13d5b-143">Keine</span><span class="sxs-lookup"><span data-stu-id="13d5b-143">None</span></span>

## <span data-ttu-id="13d5b-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="13d5b-144">OUTPUTS</span></span>

### <span data-ttu-id="13d5b-145">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="13d5b-145">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="13d5b-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="13d5b-146">NOTES</span></span>

## <span data-ttu-id="13d5b-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="13d5b-147">RELATED LINKS</span></span>

[<span data-ttu-id="13d5b-148">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="13d5b-148">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="13d5b-149">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="13d5b-149">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="13d5b-150">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="13d5b-150">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="13d5b-151">Satz-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="13d5b-151">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


