---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
ms.openlocfilehash: f4c4ccdce719b3593968f0429d5e02936d052cc4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849603"
---
# <span data-ttu-id="b7a6d-101">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b7a6d-101">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="b7a6d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b7a6d-102">SYNOPSIS</span></span>
<span data-ttu-id="b7a6d-103">Erstellt Back-End-HTTP-Einstellungen für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="b7a6d-103">Creates back-end HTTP settings for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7a6d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7a6d-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayBackendHttpSettings -Name <String> -Port <Int32> -Protocol <String>
 -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-ProbeEnabled]
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7a6d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b7a6d-105">DESCRIPTION</span></span>
<span data-ttu-id="b7a6d-106">Das New-AzureRmApplicationGatewayBackendHttpSettings-Cmdlet erstellt Back-End-HTTP-Einstellungen für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="b7a6d-106">The New-AzureRmApplicationGatewayBackendHttpSettings cmdlet creates back-end HTTP settings for an application gateway.</span></span>
<span data-ttu-id="b7a6d-107">Back-End-HTTP-Einstellungen werden auf alle Back-End-Server in einem Pool angewendet.</span><span class="sxs-lookup"><span data-stu-id="b7a6d-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="b7a6d-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b7a6d-108">EXAMPLES</span></span>

### <span data-ttu-id="b7a6d-109">Beispiel 1: Erstellen von Back-End-HTTP-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="b7a6d-109">Example 1: Create back-end HTTP settings</span></span>
```
PS C:\>$Setting = New-AzureRmApplicationGatewayBackendHttpSettings -Name "Setting01" -Port 80 -Protocol Http -CookieBasedAffinity Disabled
```

<span data-ttu-id="b7a6d-110">Dieser Befehl erstellt HTTP-Back-End-Einstellungen mit dem Namen Setting01 auf Port 80 unter Verwendung des HTTP-Protokolls mit deaktivierter Cookie-basierter Affinität.</span><span class="sxs-lookup"><span data-stu-id="b7a6d-110">This command creates back-end HTTP settings named Setting01 on port 80, using the HTTP protocol, with cookie-based affinity disabled.</span></span>
<span data-ttu-id="b7a6d-111">Die Einstellungen werden in der $Setting-Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b7a6d-111">The settings are stored in the $Setting variable.</span></span>

## <span data-ttu-id="b7a6d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7a6d-112">PARAMETERS</span></span>

### <span data-ttu-id="b7a6d-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="b7a6d-113">-AffinityCookieName</span></span>
<span data-ttu-id="b7a6d-114">Für das Affinitäts Cookie zu verwendender Cookie-Name</span><span class="sxs-lookup"><span data-stu-id="b7a6d-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="b7a6d-115">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="b7a6d-115">-AuthenticationCertificates</span></span>
<span data-ttu-id="b7a6d-116">Gibt Authentifizierungszertifikate für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="b7a6d-116">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="b7a6d-117">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="b7a6d-117">-ConnectionDraining</span></span>
<span data-ttu-id="b7a6d-118">Verbindungs Entleerung der HTTP-Back-End-Einstellungen-Ressource.</span><span class="sxs-lookup"><span data-stu-id="b7a6d-118">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="b7a6d-119">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="b7a6d-119">-CookieBasedAffinity</span></span>
<span data-ttu-id="b7a6d-120">Gibt an, ob die auf Cookies basierende Affinität für den Back-End-Serverpool aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b7a6d-120">Specifies whether cookie-based affinity should be enabled or disabled for the back-end server pool.</span></span>

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

### <span data-ttu-id="b7a6d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7a6d-121">-DefaultProfile</span></span>
<span data-ttu-id="b7a6d-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b7a6d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7a6d-123">-Hostname</span><span class="sxs-lookup"><span data-stu-id="b7a6d-123">-HostName</span></span>
<span data-ttu-id="b7a6d-124">Legt fest, dass der Hostheader an die Back-End-Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="b7a6d-124">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="b7a6d-125">-Name</span><span class="sxs-lookup"><span data-stu-id="b7a6d-125">-Name</span></span>
<span data-ttu-id="b7a6d-126">Gibt den Namen der vom Cmdlet erstellten Back-End-HTTP-Einstellungen an.</span><span class="sxs-lookup"><span data-stu-id="b7a6d-126">Specifies the name of the back-end HTTP settings that this cmdlet creates.</span></span>

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

### <span data-ttu-id="b7a6d-127">-Path</span><span class="sxs-lookup"><span data-stu-id="b7a6d-127">-Path</span></span>
<span data-ttu-id="b7a6d-128">Path, der als Präfix für alle HTTP-Anforderungen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b7a6d-128">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="b7a6d-129">Wenn für diesen Parameter kein Wert angegeben wird, wird kein Pfad mit einem Präfix versehen.</span><span class="sxs-lookup"><span data-stu-id="b7a6d-129">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="b7a6d-130">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="b7a6d-130">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="b7a6d-131">Flag, wenn der Hostheader aus dem Hostnamen des Back-End-Servers ausgewählt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b7a6d-131">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="b7a6d-132">-Port</span><span class="sxs-lookup"><span data-stu-id="b7a6d-132">-Port</span></span>
<span data-ttu-id="b7a6d-133">Gibt den Port des Back-End-Server Pools an.</span><span class="sxs-lookup"><span data-stu-id="b7a6d-133">Specifies the port of the back-end server pool.</span></span>

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

### <span data-ttu-id="b7a6d-134">-Sonde</span><span class="sxs-lookup"><span data-stu-id="b7a6d-134">-Probe</span></span>
<span data-ttu-id="b7a6d-135">Gibt einen Prüfpunkt an, der dem Back-End-Serverpool zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b7a6d-135">Specifies a probe to associate with the back-end server pool.</span></span>

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

### <span data-ttu-id="b7a6d-136">-ProbeEnabled</span><span class="sxs-lookup"><span data-stu-id="b7a6d-136">-ProbeEnabled</span></span>
<span data-ttu-id="b7a6d-137">Flag, wenn Prüfpunkt aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b7a6d-137">Flag if probe should be enabled.</span></span>

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

### <span data-ttu-id="b7a6d-138">-Sonde</span><span class="sxs-lookup"><span data-stu-id="b7a6d-138">-ProbeId</span></span>
<span data-ttu-id="b7a6d-139">Gibt die ID des Prüfpunkts an, der dem Back-End-Serverpool zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b7a6d-139">Specifies the ID of the probe to associate with the back-end server pool.</span></span>

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

### <span data-ttu-id="b7a6d-140">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="b7a6d-140">-Protocol</span></span>
<span data-ttu-id="b7a6d-141">Gibt das Protokoll an, das für die Kommunikation zwischen dem Anwendungsgateway und den Back-End-Servern verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b7a6d-141">Specifies the protocol to use for communication between the application gateway and the back-end servers.</span></span>
<span data-ttu-id="b7a6d-142">Die zulässigen Werte für diesen Parameter lauten: http und HTTPS.</span><span class="sxs-lookup"><span data-stu-id="b7a6d-142">The acceptable values for this parameter are: Http and Https.</span></span>

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

### <span data-ttu-id="b7a6d-143">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="b7a6d-143">-RequestTimeout</span></span>
<span data-ttu-id="b7a6d-144">Gibt einen Anforderungstimeout Wert an.</span><span class="sxs-lookup"><span data-stu-id="b7a6d-144">Specifies a request time-out value.</span></span>

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

### <span data-ttu-id="b7a6d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7a6d-145">CommonParameters</span></span>
<span data-ttu-id="b7a6d-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7a6d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7a6d-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7a6d-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7a6d-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b7a6d-148">INPUTS</span></span>

### <span data-ttu-id="b7a6d-149">System. String</span><span class="sxs-lookup"><span data-stu-id="b7a6d-149">System.String</span></span>

## <span data-ttu-id="b7a6d-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b7a6d-150">OUTPUTS</span></span>

### <span data-ttu-id="b7a6d-151">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b7a6d-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="b7a6d-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="b7a6d-152">NOTES</span></span>

## <span data-ttu-id="b7a6d-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b7a6d-153">RELATED LINKS</span></span>

[<span data-ttu-id="b7a6d-154">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b7a6d-154">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="b7a6d-155">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b7a6d-155">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="b7a6d-156">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b7a6d-156">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="b7a6d-157">Satz-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="b7a6d-157">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

