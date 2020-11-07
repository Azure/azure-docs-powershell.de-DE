---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 014309ceb54b1d16b2a55c97b03887deaf4ef281
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660636"
---
# <span data-ttu-id="69105-101">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="69105-101">New-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="69105-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="69105-102">SYNOPSIS</span></span>
<span data-ttu-id="69105-103">Erstellt eine Back-End-HTTP-Einstellung für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="69105-103">Creates back-end HTTP setting for an application gateway.</span></span>

## <span data-ttu-id="69105-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="69105-104">SYNTAX</span></span>

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

## <span data-ttu-id="69105-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="69105-105">DESCRIPTION</span></span>
<span data-ttu-id="69105-106">Das New-AzApplicationGatewayBackendHttpSetting-Cmdlet erstellt Back-End-HTTP-Einstellungen für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="69105-106">The New-AzApplicationGatewayBackendHttpSetting cmdlet creates back-end HTTP settings for an application gateway.</span></span>
<span data-ttu-id="69105-107">Back-End-HTTP-Einstellungen werden auf alle Back-End-Server in einem Pool angewendet.</span><span class="sxs-lookup"><span data-stu-id="69105-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="69105-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="69105-108">EXAMPLES</span></span>

### <span data-ttu-id="69105-109">Beispiel 1: Erstellen von Back-End-HTTP-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="69105-109">Example 1: Create back-end HTTP settings</span></span>
```
PS C:\>$Setting = New-AzApplicationGatewayBackendHttpSetting -Name "Setting01" -Port 80 -Protocol Http -CookieBasedAffinity Disabled
```

<span data-ttu-id="69105-110">Dieser Befehl erstellt HTTP-Back-End-Einstellungen mit dem Namen Setting01 auf Port 80 unter Verwendung des HTTP-Protokolls mit deaktivierter Cookie-basierter Affinität.</span><span class="sxs-lookup"><span data-stu-id="69105-110">This command creates back-end HTTP settings named Setting01 on port 80, using the HTTP protocol, with cookie-based affinity disabled.</span></span>
<span data-ttu-id="69105-111">Die Einstellungen werden in der $Setting-Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="69105-111">The settings are stored in the $Setting variable.</span></span>

## <span data-ttu-id="69105-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="69105-112">PARAMETERS</span></span>

### <span data-ttu-id="69105-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="69105-113">-AffinityCookieName</span></span>
<span data-ttu-id="69105-114">Für das Affinitäts Cookie zu verwendender Cookie-Name</span><span class="sxs-lookup"><span data-stu-id="69105-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="69105-115">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="69105-115">-AuthenticationCertificates</span></span>
<span data-ttu-id="69105-116">Gibt Authentifizierungszertifikate für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="69105-116">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="69105-117">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="69105-117">-ConnectionDraining</span></span>
<span data-ttu-id="69105-118">Verbindungs Entleerung der HTTP-Back-End-Einstellungen-Ressource.</span><span class="sxs-lookup"><span data-stu-id="69105-118">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="69105-119">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="69105-119">-CookieBasedAffinity</span></span>
<span data-ttu-id="69105-120">Gibt an, ob die auf Cookies basierende Affinität für den Back-End-Serverpool aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="69105-120">Specifies whether cookie-based affinity should be enabled or disabled for the back-end server pool.</span></span>

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

### <span data-ttu-id="69105-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69105-121">-DefaultProfile</span></span>
<span data-ttu-id="69105-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="69105-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69105-123">-Hostname</span><span class="sxs-lookup"><span data-stu-id="69105-123">-HostName</span></span>
<span data-ttu-id="69105-124">Legt fest, dass der Hostheader an die Back-End-Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="69105-124">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="69105-125">-Name</span><span class="sxs-lookup"><span data-stu-id="69105-125">-Name</span></span>
<span data-ttu-id="69105-126">Gibt den Namen der vom Cmdlet erstellten Back-End-HTTP-Einstellungen an.</span><span class="sxs-lookup"><span data-stu-id="69105-126">Specifies the name of the back-end HTTP settings that this cmdlet creates.</span></span>

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

### <span data-ttu-id="69105-127">-Path</span><span class="sxs-lookup"><span data-stu-id="69105-127">-Path</span></span>
<span data-ttu-id="69105-128">Path, der als Präfix für alle HTTP-Anforderungen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="69105-128">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="69105-129">Wenn für diesen Parameter kein Wert angegeben wird, wird kein Pfad mit einem Präfix versehen.</span><span class="sxs-lookup"><span data-stu-id="69105-129">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="69105-130">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="69105-130">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="69105-131">Flag, wenn der Hostheader aus dem Hostnamen des Back-End-Servers ausgewählt werden soll.</span><span class="sxs-lookup"><span data-stu-id="69105-131">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="69105-132">-Port</span><span class="sxs-lookup"><span data-stu-id="69105-132">-Port</span></span>
<span data-ttu-id="69105-133">Gibt den Port des Back-End-Server Pools an.</span><span class="sxs-lookup"><span data-stu-id="69105-133">Specifies the port of the back-end server pool.</span></span>

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

### <span data-ttu-id="69105-134">-Sonde</span><span class="sxs-lookup"><span data-stu-id="69105-134">-Probe</span></span>
<span data-ttu-id="69105-135">Gibt einen Prüfpunkt an, der dem Back-End-Serverpool zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="69105-135">Specifies a probe to associate with the back-end server pool.</span></span>

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

### <span data-ttu-id="69105-136">-Sonde</span><span class="sxs-lookup"><span data-stu-id="69105-136">-ProbeId</span></span>
<span data-ttu-id="69105-137">Gibt die ID des Prüfpunkts an, der dem Back-End-Serverpool zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="69105-137">Specifies the ID of the probe to associate with the back-end server pool.</span></span>

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

### <span data-ttu-id="69105-138">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="69105-138">-Protocol</span></span>
<span data-ttu-id="69105-139">Gibt das Protokoll an, das für die Kommunikation zwischen dem Anwendungsgateway und den Back-End-Servern verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="69105-139">Specifies the protocol to use for communication between the application gateway and the back-end servers.</span></span>
<span data-ttu-id="69105-140">Die zulässigen Werte für diesen Parameter lauten: http und HTTPS.</span><span class="sxs-lookup"><span data-stu-id="69105-140">The acceptable values for this parameter are: Http and Https.</span></span>

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

### <span data-ttu-id="69105-141">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="69105-141">-RequestTimeout</span></span>
<span data-ttu-id="69105-142">Gibt einen Anforderungstimeout Wert an.</span><span class="sxs-lookup"><span data-stu-id="69105-142">Specifies a request time-out value.</span></span>

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

### <span data-ttu-id="69105-143">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="69105-143">-TrustedRootCertificate</span></span>
<span data-ttu-id="69105-144">Vertrauenswürdige Stammzertifikate des Anwendungs Gateways</span><span class="sxs-lookup"><span data-stu-id="69105-144">Application gateway Trusted Root Certificates</span></span>

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

### <span data-ttu-id="69105-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69105-145">CommonParameters</span></span>
<span data-ttu-id="69105-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69105-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69105-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69105-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69105-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="69105-148">INPUTS</span></span>

### <span data-ttu-id="69105-149">Keine</span><span class="sxs-lookup"><span data-stu-id="69105-149">None</span></span>

## <span data-ttu-id="69105-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="69105-150">OUTPUTS</span></span>

### <span data-ttu-id="69105-151">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="69105-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="69105-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="69105-152">NOTES</span></span>

## <span data-ttu-id="69105-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="69105-153">RELATED LINKS</span></span>

[<span data-ttu-id="69105-154">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="69105-154">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="69105-155">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="69105-155">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="69105-156">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="69105-156">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="69105-157">Satz-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="69105-157">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

