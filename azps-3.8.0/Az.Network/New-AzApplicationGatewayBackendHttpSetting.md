---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: e3dc6589ae3ba72140e0fa95ceec98ab280937f8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94005048"
---
# <span data-ttu-id="1025a-101">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="1025a-101">New-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="1025a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1025a-102">SYNOPSIS</span></span>
<span data-ttu-id="1025a-103">Erstellt eine Back-End-HTTP-Einstellung für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="1025a-103">Creates back-end HTTP setting for an application gateway.</span></span>

## <span data-ttu-id="1025a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1025a-104">SYNTAX</span></span>

```
New-AzApplicationGatewayBackendHttpSetting -Name <String> -Port <Int32> -Protocol <String>
 -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>] [-PickHostNameFromBackendAddress]
 [-HostName <String>] [-AffinityCookieName <String>] [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1025a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1025a-105">DESCRIPTION</span></span>
<span data-ttu-id="1025a-106">Das New-AzApplicationGatewayBackendHttpSetting-Cmdlet erstellt Back-End-HTTP-Einstellungen für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="1025a-106">The New-AzApplicationGatewayBackendHttpSetting cmdlet creates back-end HTTP settings for an application gateway.</span></span>
<span data-ttu-id="1025a-107">Back-End-HTTP-Einstellungen werden auf alle Back-End-Server in einem Pool angewendet.</span><span class="sxs-lookup"><span data-stu-id="1025a-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="1025a-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1025a-108">EXAMPLES</span></span>

### <span data-ttu-id="1025a-109">Beispiel 1: Erstellen von Back-End-HTTP-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="1025a-109">Example 1: Create back-end HTTP settings</span></span>
```
PS C:\>$Setting = New-AzApplicationGatewayBackendHttpSetting -Name "Setting01" -Port 80 -Protocol Http -CookieBasedAffinity Disabled
```

<span data-ttu-id="1025a-110">Dieser Befehl erstellt HTTP-Back-End-Einstellungen mit dem Namen Setting01 auf Port 80 unter Verwendung des HTTP-Protokolls mit deaktivierter Cookie-basierter Affinität.</span><span class="sxs-lookup"><span data-stu-id="1025a-110">This command creates back-end HTTP settings named Setting01 on port 80, using the HTTP protocol, with cookie-based affinity disabled.</span></span>
<span data-ttu-id="1025a-111">Die Einstellungen werden in der $Setting-Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1025a-111">The settings are stored in the $Setting variable.</span></span>

## <span data-ttu-id="1025a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1025a-112">PARAMETERS</span></span>

### <span data-ttu-id="1025a-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="1025a-113">-AffinityCookieName</span></span>
<span data-ttu-id="1025a-114">Für das Affinitäts Cookie zu verwendender Cookie-Name</span><span class="sxs-lookup"><span data-stu-id="1025a-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="1025a-115">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="1025a-115">-AuthenticationCertificates</span></span>
<span data-ttu-id="1025a-116">Gibt Authentifizierungszertifikate für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="1025a-116">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="1025a-117">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="1025a-117">-ConnectionDraining</span></span>
<span data-ttu-id="1025a-118">Verbindungs Entleerung der HTTP-Back-End-Einstellungen-Ressource.</span><span class="sxs-lookup"><span data-stu-id="1025a-118">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="1025a-119">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="1025a-119">-CookieBasedAffinity</span></span>
<span data-ttu-id="1025a-120">Gibt an, ob die auf Cookies basierende Affinität für den Back-End-Serverpool aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1025a-120">Specifies whether cookie-based affinity should be enabled or disabled for the back-end server pool.</span></span>

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

### <span data-ttu-id="1025a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1025a-121">-DefaultProfile</span></span>
<span data-ttu-id="1025a-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1025a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1025a-123">-Hostname</span><span class="sxs-lookup"><span data-stu-id="1025a-123">-HostName</span></span>
<span data-ttu-id="1025a-124">Legt fest, dass der Hostheader an die Back-End-Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="1025a-124">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="1025a-125">-Name</span><span class="sxs-lookup"><span data-stu-id="1025a-125">-Name</span></span>
<span data-ttu-id="1025a-126">Gibt den Namen der vom Cmdlet erstellten Back-End-HTTP-Einstellungen an.</span><span class="sxs-lookup"><span data-stu-id="1025a-126">Specifies the name of the back-end HTTP settings that this cmdlet creates.</span></span>

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

### <span data-ttu-id="1025a-127">-Path</span><span class="sxs-lookup"><span data-stu-id="1025a-127">-Path</span></span>
<span data-ttu-id="1025a-128">Path, der als Präfix für alle HTTP-Anforderungen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1025a-128">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="1025a-129">Wenn für diesen Parameter kein Wert angegeben wird, wird kein Pfad mit einem Präfix versehen.</span><span class="sxs-lookup"><span data-stu-id="1025a-129">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="1025a-130">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="1025a-130">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="1025a-131">Flag, wenn der Hostheader aus dem Hostnamen des Back-End-Servers ausgewählt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1025a-131">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="1025a-132">-Port</span><span class="sxs-lookup"><span data-stu-id="1025a-132">-Port</span></span>
<span data-ttu-id="1025a-133">Gibt den Port des Back-End-Server Pools an.</span><span class="sxs-lookup"><span data-stu-id="1025a-133">Specifies the port of the back-end server pool.</span></span>

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

### <span data-ttu-id="1025a-134">-Sonde</span><span class="sxs-lookup"><span data-stu-id="1025a-134">-Probe</span></span>
<span data-ttu-id="1025a-135">Gibt einen Prüfpunkt an, der dem Back-End-Serverpool zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1025a-135">Specifies a probe to associate with the back-end server pool.</span></span>

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

### <span data-ttu-id="1025a-136">-Sonde</span><span class="sxs-lookup"><span data-stu-id="1025a-136">-ProbeId</span></span>
<span data-ttu-id="1025a-137">Gibt die ID des Prüfpunkts an, der dem Back-End-Serverpool zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1025a-137">Specifies the ID of the probe to associate with the back-end server pool.</span></span>

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

### <span data-ttu-id="1025a-138">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="1025a-138">-Protocol</span></span>
<span data-ttu-id="1025a-139">Gibt das Protokoll an, das für die Kommunikation zwischen dem Anwendungsgateway und den Back-End-Servern verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1025a-139">Specifies the protocol to use for communication between the application gateway and the back-end servers.</span></span>
<span data-ttu-id="1025a-140">Die zulässigen Werte für diesen Parameter lauten: http und HTTPS.</span><span class="sxs-lookup"><span data-stu-id="1025a-140">The acceptable values for this parameter are: Http and Https.</span></span>

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

### <span data-ttu-id="1025a-141">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="1025a-141">-RequestTimeout</span></span>
<span data-ttu-id="1025a-142">Gibt einen Anforderungstimeout Wert an.</span><span class="sxs-lookup"><span data-stu-id="1025a-142">Specifies a request time-out value.</span></span>

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

### <span data-ttu-id="1025a-143">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="1025a-143">-TrustedRootCertificate</span></span>
<span data-ttu-id="1025a-144">Vertrauenswürdige Stammzertifikate des Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="1025a-144">Application gateway Trusted Root Certificates</span></span>

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

### <span data-ttu-id="1025a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1025a-145">CommonParameters</span></span>
<span data-ttu-id="1025a-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1025a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1025a-147">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1025a-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1025a-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1025a-148">INPUTS</span></span>

### <span data-ttu-id="1025a-149">Keine</span><span class="sxs-lookup"><span data-stu-id="1025a-149">None</span></span>

## <span data-ttu-id="1025a-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1025a-150">OUTPUTS</span></span>

### <span data-ttu-id="1025a-151">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="1025a-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="1025a-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="1025a-152">NOTES</span></span>

## <span data-ttu-id="1025a-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1025a-153">RELATED LINKS</span></span>

[<span data-ttu-id="1025a-154">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="1025a-154">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="1025a-155">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="1025a-155">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="1025a-156">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="1025a-156">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="1025a-157">Satz-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="1025a-157">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

