---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-AzApplicationGatewayBackendHttpSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 4361d025026e3ff9c9a72a092a99a72b8b63c850
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841884"
---
# <span data-ttu-id="17b2d-101">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="17b2d-101">Add-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="17b2d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="17b2d-102">SYNOPSIS</span></span>
<span data-ttu-id="17b2d-103">Fügt einem Anwendungsgateway http-Einstellungen für das Back-End hinzu.</span><span class="sxs-lookup"><span data-stu-id="17b2d-103">Adds back-end HTTP settings to an application gateway.</span></span>

## <span data-ttu-id="17b2d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="17b2d-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayBackendHttpSetting -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-ProbeEnabled]
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17b2d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="17b2d-105">DESCRIPTION</span></span>
<span data-ttu-id="17b2d-106">Das Add-AzApplicationGatewayBackendHttpSetting-Cmdlet fügt einem Anwendungsgateway http-Einstellungen für das Back-End hinzu.</span><span class="sxs-lookup"><span data-stu-id="17b2d-106">The Add-AzApplicationGatewayBackendHttpSetting cmdlet adds back-end HTTP settings to an application gateway.</span></span>

<span data-ttu-id="17b2d-107">Back-End-HTTP-Einstellungen werden auf alle Back-End-Server im Pool angewendet.</span><span class="sxs-lookup"><span data-stu-id="17b2d-107">Back-end HTTP settings are applied to all back-end servers in the pool.</span></span>

## <span data-ttu-id="17b2d-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="17b2d-108">EXAMPLES</span></span>

### <span data-ttu-id="17b2d-109">Beispiel 1: Hinzufügen von Back-End-HTTP-Einstellungen zu einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="17b2d-109">Example 1: Add back-end HTTP settings to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "HTTP" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="17b2d-110">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $AppGw Variablen. Der zweite Befehl fügt dem Anwendungsgateway Back-End-HTTP-Einstellungen hinzu, legt den Port auf 88 und das Protokoll für http fest und benennt die Einstellungen Setting02.</span><span class="sxs-lookup"><span data-stu-id="17b2d-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.The second command adds back-end HTTP settings to the application gateway, setting the port to 88 and the protocol to HTTP and names the settings Setting02.</span></span>

## <span data-ttu-id="17b2d-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="17b2d-111">PARAMETERS</span></span>

### <span data-ttu-id="17b2d-112">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="17b2d-112">-AffinityCookieName</span></span>
<span data-ttu-id="17b2d-113">Für das Affinitäts Cookie zu verwendender Cookie-Name</span><span class="sxs-lookup"><span data-stu-id="17b2d-113">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="17b2d-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="17b2d-114">-ApplicationGateway</span></span>
<span data-ttu-id="17b2d-115">Gibt den Namen des Anwendungs Gateways an, für das dieses Cmdlet Einstellungen hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="17b2d-115">Specifies the name of application gateway for which this cmdlet adds settings.</span></span>

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

### <span data-ttu-id="17b2d-116">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="17b2d-116">-AuthenticationCertificates</span></span>
<span data-ttu-id="17b2d-117">Gibt Authentifizierungszertifikate für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="17b2d-117">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17b2d-118">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="17b2d-118">-ConnectionDraining</span></span>
<span data-ttu-id="17b2d-119">Verbindungs Entleerung der HTTP-Back-End-Einstellungen-Ressource.</span><span class="sxs-lookup"><span data-stu-id="17b2d-119">Connection draining of the backend http settings resource.</span></span>

```yaml
Type: PSApplicationGatewayConnectionDraining
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17b2d-120">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="17b2d-120">-CookieBasedAffinity</span></span>
<span data-ttu-id="17b2d-121">Gibt an, ob die Cookie-basierte Affinität für den Back-End-Serverpool aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="17b2d-121">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="17b2d-122">Die zulässigen Werte für diesen Parameter sind: Disabled, aktiviert.</span><span class="sxs-lookup"><span data-stu-id="17b2d-122">The acceptable values for this parameter are: Disabled, Enabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17b2d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17b2d-123">-DefaultProfile</span></span>
<span data-ttu-id="17b2d-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="17b2d-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17b2d-125">-Hostname</span><span class="sxs-lookup"><span data-stu-id="17b2d-125">-HostName</span></span>
<span data-ttu-id="17b2d-126">Legt fest, dass der Hostheader an die Back-End-Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="17b2d-126">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="17b2d-127">-Name</span><span class="sxs-lookup"><span data-stu-id="17b2d-127">-Name</span></span>
<span data-ttu-id="17b2d-128">Gibt den Namen der vom Cmdlet hinzugefügten Back-End-HTTP-Einstellungen an.</span><span class="sxs-lookup"><span data-stu-id="17b2d-128">Specifies the name of the back-end HTTP settings which this cmdlet adds.</span></span>

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

### <span data-ttu-id="17b2d-129">-Path</span><span class="sxs-lookup"><span data-stu-id="17b2d-129">-Path</span></span>
<span data-ttu-id="17b2d-130">Path, der als Präfix für alle HTTP-Anforderungen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="17b2d-130">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="17b2d-131">Wenn für diesen Parameter kein Wert angegeben wird, wird kein Pfad mit einem Präfix versehen.</span><span class="sxs-lookup"><span data-stu-id="17b2d-131">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="17b2d-132">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="17b2d-132">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="17b2d-133">Flag, wenn der Hostheader aus dem Hostnamen des Back-End-Servers ausgewählt werden soll.</span><span class="sxs-lookup"><span data-stu-id="17b2d-133">Flag if host header should be picked from the host name of the backend server.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17b2d-134">-Port</span><span class="sxs-lookup"><span data-stu-id="17b2d-134">-Port</span></span>
<span data-ttu-id="17b2d-135">Gibt den Port des Back-End-Server Pools an.</span><span class="sxs-lookup"><span data-stu-id="17b2d-135">Specifies the port of the back-end server pool.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17b2d-136">-Sonde</span><span class="sxs-lookup"><span data-stu-id="17b2d-136">-Probe</span></span>
<span data-ttu-id="17b2d-137">Gibt einen Prüfpunkt an, der einem Back-End-Server zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="17b2d-137">Specifies a probe to associate with a back-end server.</span></span>

```yaml
Type: PSApplicationGatewayProbe
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17b2d-138">-ProbeEnabled</span><span class="sxs-lookup"><span data-stu-id="17b2d-138">-ProbeEnabled</span></span>
<span data-ttu-id="17b2d-139">Flag, wenn Prüfpunkt aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="17b2d-139">Flag if probe should be enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17b2d-140">-Sonde</span><span class="sxs-lookup"><span data-stu-id="17b2d-140">-ProbeId</span></span>
<span data-ttu-id="17b2d-141">Gibt die ID des Prüfpunkts an, der dem Back-End-Server zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="17b2d-141">Specifies the ID of the probe to associate with the back-end server.</span></span>

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

### <span data-ttu-id="17b2d-142">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="17b2d-142">-Protocol</span></span>
<span data-ttu-id="17b2d-143">Gibt das Protokoll für die Kommunikation zwischen Application Gateway und Back-End-Servern an.</span><span class="sxs-lookup"><span data-stu-id="17b2d-143">Specifies the protocol for communication between application gateway and back-end servers.</span></span>
<span data-ttu-id="17b2d-144">Die zulässigen Werte für diesen Parameter lauten: http und HTTPS.</span><span class="sxs-lookup"><span data-stu-id="17b2d-144">The acceptable values for this parameter are: Http and Https.</span></span>

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

### <span data-ttu-id="17b2d-145">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="17b2d-145">-RequestTimeout</span></span>
<span data-ttu-id="17b2d-146">Gibt den Anforderungstimeout Wert an.</span><span class="sxs-lookup"><span data-stu-id="17b2d-146">Specifies the request time-out value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17b2d-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17b2d-147">CommonParameters</span></span>
<span data-ttu-id="17b2d-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17b2d-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17b2d-149">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17b2d-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17b2d-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="17b2d-150">INPUTS</span></span>

### <span data-ttu-id="17b2d-151">System. String</span><span class="sxs-lookup"><span data-stu-id="17b2d-151">System.String</span></span>

## <span data-ttu-id="17b2d-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="17b2d-152">OUTPUTS</span></span>

### <span data-ttu-id="17b2d-153">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="17b2d-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="17b2d-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="17b2d-154">NOTES</span></span>

## <span data-ttu-id="17b2d-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="17b2d-155">RELATED LINKS</span></span>

[<span data-ttu-id="17b2d-156">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="17b2d-156">Get-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="17b2d-157">Neu – AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="17b2d-157">New-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="17b2d-158">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="17b2d-158">Remove-AzApplicationGatewayBackendHttpSetting</span></span>]()

[<span data-ttu-id="17b2d-159">Satz-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="17b2d-159">Set-AzApplicationGatewayBackendHttpSetting</span></span>]()

