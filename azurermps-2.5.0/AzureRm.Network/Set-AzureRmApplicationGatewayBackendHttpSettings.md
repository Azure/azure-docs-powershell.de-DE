---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
ms.openlocfilehash: c20faf9ca89892d952d553d0f85cfa28b90ac590
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849099"
---
# <span data-ttu-id="e62a3-101">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e62a3-101">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="e62a3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e62a3-102">SYNOPSIS</span></span>
<span data-ttu-id="e62a3-103">Aktualisiert die Back-End-HTTP-Einstellungen für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="e62a3-103">Updates back-end HTTP settings for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e62a3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e62a3-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-ProbeEnabled]
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e62a3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e62a3-105">DESCRIPTION</span></span>
<span data-ttu-id="e62a3-106">Das Set-AzureRmApplicationGatewayBackendHttpSettings-Cmdlet aktualisiert die http-Einstellungen (Back-End-Hypertext Transfer Protocol) für ein Azure Application-Gateway.</span><span class="sxs-lookup"><span data-stu-id="e62a3-106">The Set-AzureRmApplicationGatewayBackendHttpSettings cmdlet updates the back-end Hypertext Transfer Protocol (HTTP) settings for an Azure application gateway.</span></span>
<span data-ttu-id="e62a3-107">Back-End-HTTP-Einstellungen werden auf alle Back-End-Server in einem Pool angewendet.</span><span class="sxs-lookup"><span data-stu-id="e62a3-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="e62a3-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e62a3-108">EXAMPLES</span></span>

### <span data-ttu-id="e62a3-109">Beispiel 1: Aktualisieren der Back-End-HTTP-Einstellungen für ein Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="e62a3-109">Example 1: Update the back-end HTTP settings for an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "Http" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="e62a3-110">Der erste Befehl ruft das Anwendungsgateway mit dem Namen ApplicationGateway01 ab, das zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert es in der $AppGw Variablen.</span><span class="sxs-lookup"><span data-stu-id="e62a3-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="e62a3-111">Der zweite Befehl aktualisiert die http-Einstellungen des Application-Gateways in der $AppGw-Variable, um Port 88, das HTTP-Protokoll, zu verwenden, und ermöglicht eine auf Cookies basierende Affinität.</span><span class="sxs-lookup"><span data-stu-id="e62a3-111">The second command updates the HTTP settings of the application gateway in the $AppGw variable to use port 88, the HTTP protocol and enables cookie-based affinity.</span></span>

## <span data-ttu-id="e62a3-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e62a3-112">PARAMETERS</span></span>

### <span data-ttu-id="e62a3-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="e62a3-113">-AffinityCookieName</span></span>
<span data-ttu-id="e62a3-114">Für das Affinitäts Cookie zu verwendender Cookie-Name</span><span class="sxs-lookup"><span data-stu-id="e62a3-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="e62a3-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e62a3-115">-ApplicationGateway</span></span>
<span data-ttu-id="e62a3-116">Gibt ein Application Gateway-Objekt an, mit dem dieses Cmdlet Back-End-HTTP-Einstellungen verknüpft.</span><span class="sxs-lookup"><span data-stu-id="e62a3-116">Specifies an application gateway object with which this cmdlet associates back-end HTTP settings.</span></span>

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

### <span data-ttu-id="e62a3-117">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="e62a3-117">-AuthenticationCertificates</span></span>
<span data-ttu-id="e62a3-118">Gibt Authentifizierungszertifikate für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="e62a3-118">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="e62a3-119">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="e62a3-119">-ConnectionDraining</span></span>
<span data-ttu-id="e62a3-120">Verbindungs Entleerung der HTTP-Back-End-Einstellungen-Ressource.</span><span class="sxs-lookup"><span data-stu-id="e62a3-120">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="e62a3-121">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="e62a3-121">-CookieBasedAffinity</span></span>
<span data-ttu-id="e62a3-122">Gibt an, ob die Cookie-basierte Affinität für den Back-End-Serverpool aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e62a3-122">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="e62a3-123">Die akzeptablen Werte für diesen Parameter sind: Disabled oder Enabled.</span><span class="sxs-lookup"><span data-stu-id="e62a3-123">The acceptable values for this parameter are: Disabled or Enabled.</span></span>

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

### <span data-ttu-id="e62a3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e62a3-124">-DefaultProfile</span></span>
<span data-ttu-id="e62a3-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e62a3-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e62a3-126">-Hostname</span><span class="sxs-lookup"><span data-stu-id="e62a3-126">-HostName</span></span>
<span data-ttu-id="e62a3-127">Legt fest, dass der Hostheader an die Back-End-Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="e62a3-127">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="e62a3-128">-Name</span><span class="sxs-lookup"><span data-stu-id="e62a3-128">-Name</span></span>
<span data-ttu-id="e62a3-129">Gibt den Namen des Back-End-HTTP-Einstellungs Objekts an.</span><span class="sxs-lookup"><span data-stu-id="e62a3-129">Specifies the name of the back-end HTTP settings object.</span></span>

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

### <span data-ttu-id="e62a3-130">-Path</span><span class="sxs-lookup"><span data-stu-id="e62a3-130">-Path</span></span>
<span data-ttu-id="e62a3-131">Path, der als Präfix für alle HTTP-Anforderungen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e62a3-131">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="e62a3-132">Wenn für diesen Parameter kein Wert angegeben wird, wird kein Pfad mit einem Präfix versehen.</span><span class="sxs-lookup"><span data-stu-id="e62a3-132">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="e62a3-133">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="e62a3-133">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="e62a3-134">Flag, wenn der Hostheader aus dem Hostnamen des Back-End-Servers ausgewählt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e62a3-134">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="e62a3-135">-Port</span><span class="sxs-lookup"><span data-stu-id="e62a3-135">-Port</span></span>
<span data-ttu-id="e62a3-136">Gibt den Port an, der für jeden Server im Back-End-Serverpool verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e62a3-136">Specifies the port to use for each server in the back-end server pool.</span></span>

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

### <span data-ttu-id="e62a3-137">-Sonde</span><span class="sxs-lookup"><span data-stu-id="e62a3-137">-Probe</span></span>
<span data-ttu-id="e62a3-138">Gibt einen Prüfpunkt an, der den Back-End-HTTP-Einstellungen zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e62a3-138">Specifies a probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="e62a3-139">-ProbeEnabled</span><span class="sxs-lookup"><span data-stu-id="e62a3-139">-ProbeEnabled</span></span>
<span data-ttu-id="e62a3-140">Flag, wenn Prüfpunkt aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e62a3-140">Flag if probe should be enabled.</span></span>

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

### <span data-ttu-id="e62a3-141">-Sonde</span><span class="sxs-lookup"><span data-stu-id="e62a3-141">-ProbeId</span></span>
<span data-ttu-id="e62a3-142">Gibt die ID des Prüfpunkts an, der den Back-End-HTTP-Einstellungen zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e62a3-142">Specifies the ID of the probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="e62a3-143">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="e62a3-143">-Protocol</span></span>
<span data-ttu-id="e62a3-144">Gibt das Protokoll an, das für die Kommunikation zwischen dem Anwendungs-Gateway und den Back-End-Servern verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e62a3-144">Specifies the protocol to use for communication between the application gateway and back-end servers.</span></span>
<span data-ttu-id="e62a3-145">Die zulässigen Werte für diesen Parameter lauten: http und HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e62a3-145">The acceptable values for this parameter are: Http and Https.</span></span>
<span data-ttu-id="e62a3-146">Bei diesem Parameter wird die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="e62a3-146">This parameter is case-sensitive.</span></span>

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

### <span data-ttu-id="e62a3-147">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="e62a3-147">-RequestTimeout</span></span>
<span data-ttu-id="e62a3-148">Gibt einen Anforderungstimeout Wert an.</span><span class="sxs-lookup"><span data-stu-id="e62a3-148">Specifies a request time-out value.</span></span>

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

### <span data-ttu-id="e62a3-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e62a3-149">CommonParameters</span></span>
<span data-ttu-id="e62a3-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e62a3-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e62a3-151">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e62a3-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e62a3-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e62a3-152">INPUTS</span></span>

### <span data-ttu-id="e62a3-153">System. String</span><span class="sxs-lookup"><span data-stu-id="e62a3-153">System.String</span></span>

## <span data-ttu-id="e62a3-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e62a3-154">OUTPUTS</span></span>

### <span data-ttu-id="e62a3-155">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e62a3-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e62a3-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="e62a3-156">NOTES</span></span>

## <span data-ttu-id="e62a3-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e62a3-157">RELATED LINKS</span></span>

[<span data-ttu-id="e62a3-158">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e62a3-158">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="e62a3-159">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e62a3-159">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="e62a3-160">Neu – AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e62a3-160">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="e62a3-161">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e62a3-161">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

