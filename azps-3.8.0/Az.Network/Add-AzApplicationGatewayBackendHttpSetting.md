---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 15468a2a1c4ed339a05b8f05b6208e827a4bde72
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996084"
---
# <span data-ttu-id="5edc7-101">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="5edc7-101">Add-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="5edc7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5edc7-102">SYNOPSIS</span></span>
<span data-ttu-id="5edc7-103">Fügt einem Anwendungsgateway http-Einstellungen für das Back-End hinzu.</span><span class="sxs-lookup"><span data-stu-id="5edc7-103">Adds back-end HTTP settings to an application gateway.</span></span>

## <span data-ttu-id="5edc7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5edc7-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayBackendHttpSetting -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>] [-PickHostNameFromBackendAddress]
 [-HostName <String>] [-AffinityCookieName <String>] [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5edc7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5edc7-105">DESCRIPTION</span></span>
<span data-ttu-id="5edc7-106">Das Add-AzApplicationGatewayBackendHttpSetting-Cmdlet fügt einem Anwendungsgateway http-Einstellungen für das Back-End hinzu.</span><span class="sxs-lookup"><span data-stu-id="5edc7-106">The Add-AzApplicationGatewayBackendHttpSetting cmdlet adds back-end HTTP settings to an application gateway.</span></span>
<span data-ttu-id="5edc7-107">Back-End-HTTP-Einstellungen werden auf alle Back-End-Server im Pool angewendet.</span><span class="sxs-lookup"><span data-stu-id="5edc7-107">Back-end HTTP settings are applied to all back-end servers in the pool.</span></span>

## <span data-ttu-id="5edc7-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5edc7-108">EXAMPLES</span></span>

### <span data-ttu-id="5edc7-109">Beispiel 1: Hinzufügen von Back-End-HTTP-Einstellungen zu einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="5edc7-109">Example 1: Add back-end HTTP settings to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "HTTP" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="5edc7-110">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $AppGw Variablen. Der zweite Befehl fügt dem Anwendungsgateway Back-End-HTTP-Einstellungen hinzu, legt den Port auf 88 und das Protokoll für http fest und benennt die Einstellungen Setting02.</span><span class="sxs-lookup"><span data-stu-id="5edc7-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.The second command adds back-end HTTP settings to the application gateway, setting the port to 88 and the protocol to HTTP and names the settings Setting02.</span></span>

## <span data-ttu-id="5edc7-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="5edc7-111">PARAMETERS</span></span>

### <span data-ttu-id="5edc7-112">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="5edc7-112">-AffinityCookieName</span></span>
<span data-ttu-id="5edc7-113">Für das Affinitäts Cookie zu verwendender Cookie-Name</span><span class="sxs-lookup"><span data-stu-id="5edc7-113">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="5edc7-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5edc7-114">-ApplicationGateway</span></span>
<span data-ttu-id="5edc7-115">Gibt den Namen des Anwendungs Gateways an, für das dieses Cmdlet Einstellungen hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="5edc7-115">Specifies the name of application gateway for which this cmdlet adds settings.</span></span>

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

### <span data-ttu-id="5edc7-116">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="5edc7-116">-AuthenticationCertificates</span></span>
<span data-ttu-id="5edc7-117">Gibt Authentifizierungszertifikate für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="5edc7-117">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5edc7-118">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="5edc7-118">-ConnectionDraining</span></span>
<span data-ttu-id="5edc7-119">Verbindungs Entleerung der HTTP-Back-End-Einstellungen-Ressource.</span><span class="sxs-lookup"><span data-stu-id="5edc7-119">Connection draining of the backend http settings resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5edc7-120">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="5edc7-120">-CookieBasedAffinity</span></span>
<span data-ttu-id="5edc7-121">Gibt an, ob die Cookie-basierte Affinität für den Back-End-Serverpool aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5edc7-121">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="5edc7-122">Die zulässigen Werte für diesen Parameter sind: Disabled, aktiviert.</span><span class="sxs-lookup"><span data-stu-id="5edc7-122">The acceptable values for this parameter are: Disabled, Enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5edc7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5edc7-123">-DefaultProfile</span></span>
<span data-ttu-id="5edc7-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5edc7-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5edc7-125">-Hostname</span><span class="sxs-lookup"><span data-stu-id="5edc7-125">-HostName</span></span>
<span data-ttu-id="5edc7-126">Legt fest, dass der Hostheader an die Back-End-Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="5edc7-126">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="5edc7-127">-Name</span><span class="sxs-lookup"><span data-stu-id="5edc7-127">-Name</span></span>
<span data-ttu-id="5edc7-128">Gibt den Namen der vom Cmdlet hinzugefügten Back-End-HTTP-Einstellungen an.</span><span class="sxs-lookup"><span data-stu-id="5edc7-128">Specifies the name of the back-end HTTP settings which this cmdlet adds.</span></span>

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

### <span data-ttu-id="5edc7-129">-Path</span><span class="sxs-lookup"><span data-stu-id="5edc7-129">-Path</span></span>
<span data-ttu-id="5edc7-130">Path, der als Präfix für alle HTTP-Anforderungen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5edc7-130">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="5edc7-131">Wenn für diesen Parameter kein Wert angegeben wird, wird kein Pfad mit einem Präfix versehen.</span><span class="sxs-lookup"><span data-stu-id="5edc7-131">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="5edc7-132">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="5edc7-132">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="5edc7-133">Flag, wenn der Hostheader aus dem Hostnamen des Back-End-Servers ausgewählt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5edc7-133">Flag if host header should be picked from the host name of the backend server.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5edc7-134">-Port</span><span class="sxs-lookup"><span data-stu-id="5edc7-134">-Port</span></span>
<span data-ttu-id="5edc7-135">Gibt den Port des Back-End-Server Pools an.</span><span class="sxs-lookup"><span data-stu-id="5edc7-135">Specifies the port of the back-end server pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5edc7-136">-Sonde</span><span class="sxs-lookup"><span data-stu-id="5edc7-136">-Probe</span></span>
<span data-ttu-id="5edc7-137">Gibt einen Prüfpunkt an, der einem Back-End-Server zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5edc7-137">Specifies a probe to associate with a back-end server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5edc7-138">-Sonde</span><span class="sxs-lookup"><span data-stu-id="5edc7-138">-ProbeId</span></span>
<span data-ttu-id="5edc7-139">Gibt die ID des Prüfpunkts an, der dem Back-End-Server zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5edc7-139">Specifies the ID of the probe to associate with the back-end server.</span></span>

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

### <span data-ttu-id="5edc7-140">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="5edc7-140">-Protocol</span></span>
<span data-ttu-id="5edc7-141">Gibt das Protokoll für die Kommunikation zwischen Application Gateway und Back-End-Servern an.</span><span class="sxs-lookup"><span data-stu-id="5edc7-141">Specifies the protocol for communication between application gateway and back-end servers.</span></span>
<span data-ttu-id="5edc7-142">Die zulässigen Werte für diesen Parameter lauten: http und HTTPS.</span><span class="sxs-lookup"><span data-stu-id="5edc7-142">The acceptable values for this parameter are: Http and Https.</span></span>

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

### <span data-ttu-id="5edc7-143">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="5edc7-143">-RequestTimeout</span></span>
<span data-ttu-id="5edc7-144">Gibt den Anforderungstimeout Wert an.</span><span class="sxs-lookup"><span data-stu-id="5edc7-144">Specifies the request time-out value.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5edc7-145">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="5edc7-145">-TrustedRootCertificate</span></span>
<span data-ttu-id="5edc7-146">Vertrauenswürdige Stammzertifikate des Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="5edc7-146">Application gateway Trusted Root Certificates</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5edc7-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5edc7-147">CommonParameters</span></span>
<span data-ttu-id="5edc7-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5edc7-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5edc7-149">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5edc7-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5edc7-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5edc7-150">INPUTS</span></span>

### <span data-ttu-id="5edc7-151">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5edc7-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5edc7-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5edc7-152">OUTPUTS</span></span>

### <span data-ttu-id="5edc7-153">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5edc7-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5edc7-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="5edc7-154">NOTES</span></span>

## <span data-ttu-id="5edc7-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5edc7-155">RELATED LINKS</span></span>

[<span data-ttu-id="5edc7-156">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="5edc7-156">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="5edc7-157">Neu – AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="5edc7-157">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="5edc7-158">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="5edc7-158">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="5edc7-159">Satz-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="5edc7-159">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

