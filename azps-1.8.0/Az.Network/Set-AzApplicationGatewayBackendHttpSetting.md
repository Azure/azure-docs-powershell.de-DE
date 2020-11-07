---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: bfbd91d68bdbf1c9939ecc8637aae0314a74a4c2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660273"
---
# <span data-ttu-id="e8102-101">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="e8102-101">Set-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="e8102-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e8102-102">SYNOPSIS</span></span>
<span data-ttu-id="e8102-103">Aktualisiert die Back-End-HTTP-Einstellungen für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="e8102-103">Updates back-end HTTP settings for an application gateway.</span></span>

## <span data-ttu-id="e8102-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8102-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayBackendHttpSetting -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>] [-PickHostNameFromBackendAddress]
 [-HostName <String>] [-AffinityCookieName <String>] [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8102-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e8102-105">DESCRIPTION</span></span>
<span data-ttu-id="e8102-106">Das Set-AzApplicationGatewayBackendHttpSetting-Cmdlet aktualisiert die http-Einstellungen (Back-End-Hypertext Transfer Protocol) für ein Azure Application-Gateway.</span><span class="sxs-lookup"><span data-stu-id="e8102-106">The Set-AzApplicationGatewayBackendHttpSetting cmdlet updates the back-end Hypertext Transfer Protocol (HTTP) settings for an Azure application gateway.</span></span>
<span data-ttu-id="e8102-107">Back-End-HTTP-Einstellungen werden auf alle Back-End-Server in einem Pool angewendet.</span><span class="sxs-lookup"><span data-stu-id="e8102-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="e8102-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e8102-108">EXAMPLES</span></span>

### <span data-ttu-id="e8102-109">Beispiel 1: Aktualisieren der Back-End-HTTP-Einstellungen für ein Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="e8102-109">Example 1: Update the back-end HTTP settings for an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "Http" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="e8102-110">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="e8102-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e8102-111">Der zweite Befehl aktualisiert die http-Einstellungen des Application-Gateways in der $AppGw-Variable, um Port 88, das HTTP-Protokoll, zu verwenden, und ermöglicht eine auf Cookies basierende Affinität.</span><span class="sxs-lookup"><span data-stu-id="e8102-111">The second command updates the HTTP settings of the application gateway in the $AppGw variable to use port 88, the HTTP protocol and enables cookie-based affinity.</span></span>

## <span data-ttu-id="e8102-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8102-112">PARAMETERS</span></span>

### <span data-ttu-id="e8102-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="e8102-113">-AffinityCookieName</span></span>
<span data-ttu-id="e8102-114">Für das Affinitäts Cookie zu verwendender Cookie-Name</span><span class="sxs-lookup"><span data-stu-id="e8102-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="e8102-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e8102-115">-ApplicationGateway</span></span>
<span data-ttu-id="e8102-116">Gibt ein Application Gateway-Objekt an, mit dem dieses Cmdlet Back-End-HTTP-Einstellungen verknüpft.</span><span class="sxs-lookup"><span data-stu-id="e8102-116">Specifies an application gateway object with which this cmdlet associates back-end HTTP settings.</span></span>

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

### <span data-ttu-id="e8102-117">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="e8102-117">-AuthenticationCertificates</span></span>
<span data-ttu-id="e8102-118">Gibt Authentifizierungszertifikate für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="e8102-118">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="e8102-119">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="e8102-119">-ConnectionDraining</span></span>
<span data-ttu-id="e8102-120">Verbindungs Entleerung der HTTP-Back-End-Einstellungen-Ressource.</span><span class="sxs-lookup"><span data-stu-id="e8102-120">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="e8102-121">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="e8102-121">-CookieBasedAffinity</span></span>
<span data-ttu-id="e8102-122">Gibt an, ob die Cookie-basierte Affinität für den Back-End-Serverpool aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e8102-122">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="e8102-123">Die akzeptablen Werte für diesen Parameter sind: Disabled oder Enabled.</span><span class="sxs-lookup"><span data-stu-id="e8102-123">The acceptable values for this parameter are: Disabled or Enabled.</span></span>

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

### <span data-ttu-id="e8102-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8102-124">-DefaultProfile</span></span>
<span data-ttu-id="e8102-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e8102-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8102-126">-Hostname</span><span class="sxs-lookup"><span data-stu-id="e8102-126">-HostName</span></span>
<span data-ttu-id="e8102-127">Legt fest, dass der Hostheader an die Back-End-Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="e8102-127">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="e8102-128">-Name</span><span class="sxs-lookup"><span data-stu-id="e8102-128">-Name</span></span>
<span data-ttu-id="e8102-129">Gibt den Namen des Back-End-HTTP-Einstellungs Objekts an.</span><span class="sxs-lookup"><span data-stu-id="e8102-129">Specifies the name of the back-end HTTP settings object.</span></span>

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

### <span data-ttu-id="e8102-130">-Path</span><span class="sxs-lookup"><span data-stu-id="e8102-130">-Path</span></span>
<span data-ttu-id="e8102-131">Path, der als Präfix für alle HTTP-Anforderungen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e8102-131">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="e8102-132">Wenn für diesen Parameter kein Wert angegeben wird, wird kein Pfad mit einem Präfix versehen.</span><span class="sxs-lookup"><span data-stu-id="e8102-132">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="e8102-133">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="e8102-133">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="e8102-134">Flag, wenn der Hostheader aus dem Hostnamen des Back-End-Servers ausgewählt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e8102-134">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="e8102-135">-Port</span><span class="sxs-lookup"><span data-stu-id="e8102-135">-Port</span></span>
<span data-ttu-id="e8102-136">Gibt den Port an, der für jeden Server im Back-End-Serverpool verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e8102-136">Specifies the port to use for each server in the back-end server pool.</span></span>

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

### <span data-ttu-id="e8102-137">-Sonde</span><span class="sxs-lookup"><span data-stu-id="e8102-137">-Probe</span></span>
<span data-ttu-id="e8102-138">Gibt einen Prüfpunkt an, der den Back-End-HTTP-Einstellungen zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e8102-138">Specifies a probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="e8102-139">-Sonde</span><span class="sxs-lookup"><span data-stu-id="e8102-139">-ProbeId</span></span>
<span data-ttu-id="e8102-140">Gibt die ID des Prüfpunkts an, der den Back-End-HTTP-Einstellungen zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e8102-140">Specifies the ID of the probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="e8102-141">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="e8102-141">-Protocol</span></span>
<span data-ttu-id="e8102-142">Gibt das Protokoll an, das für die Kommunikation zwischen dem Anwendungs-Gateway und den Back-End-Servern verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e8102-142">Specifies the protocol to use for communication between the application gateway and back-end servers.</span></span>
<span data-ttu-id="e8102-143">Die zulässigen Werte für diesen Parameter lauten: http und HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e8102-143">The acceptable values for this parameter are: Http and Https.</span></span>
<span data-ttu-id="e8102-144">Bei diesem Parameter wird die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="e8102-144">This parameter is case-sensitive.</span></span>

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

### <span data-ttu-id="e8102-145">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="e8102-145">-RequestTimeout</span></span>
<span data-ttu-id="e8102-146">Gibt einen Anforderungstimeout Wert an.</span><span class="sxs-lookup"><span data-stu-id="e8102-146">Specifies a request time-out value.</span></span>

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

### <span data-ttu-id="e8102-147">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e8102-147">-TrustedRootCertificate</span></span>
<span data-ttu-id="e8102-148">Vertrauenswürdige Stammzertifikate des Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="e8102-148">Application gateway Trusted Root Certificates</span></span>

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

### <span data-ttu-id="e8102-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8102-149">CommonParameters</span></span>
<span data-ttu-id="e8102-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8102-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8102-151">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8102-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8102-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e8102-152">INPUTS</span></span>

### <span data-ttu-id="e8102-153">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e8102-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e8102-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e8102-154">OUTPUTS</span></span>

### <span data-ttu-id="e8102-155">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e8102-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e8102-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="e8102-156">NOTES</span></span>

## <span data-ttu-id="e8102-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e8102-157">RELATED LINKS</span></span>

[<span data-ttu-id="e8102-158">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="e8102-158">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="e8102-159">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="e8102-159">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="e8102-160">Neu – AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="e8102-160">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="e8102-161">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="e8102-161">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

