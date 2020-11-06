---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: 6183b3cd61380b139bd74d676c6ab5225bf338fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499954"
---
# <span data-ttu-id="7cd1c-101">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7cd1c-101">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="7cd1c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7cd1c-102">SYNOPSIS</span></span>
<span data-ttu-id="7cd1c-103">Erstellt Back-End-HTTP-Einstellungen für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="7cd1c-103">Creates back-end HTTP settings for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7cd1c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7cd1c-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayBackendHttpSettings -Name <String> -Port <Int32> -Protocol <String>
 -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-ProbeEnabled]
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7cd1c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7cd1c-105">DESCRIPTION</span></span>
<span data-ttu-id="7cd1c-106">Das New-AzureRmApplicationGatewayBackendHttpSettings-Cmdlet erstellt Back-End-HTTP-Einstellungen für ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="7cd1c-106">The New-AzureRmApplicationGatewayBackendHttpSettings cmdlet creates back-end HTTP settings for an application gateway.</span></span>
<span data-ttu-id="7cd1c-107">Back-End-HTTP-Einstellungen werden auf alle Back-End-Server in einem Pool angewendet.</span><span class="sxs-lookup"><span data-stu-id="7cd1c-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="7cd1c-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7cd1c-108">EXAMPLES</span></span>

### <span data-ttu-id="7cd1c-109">Beispiel 1: Erstellen von Back-End-HTTP-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="7cd1c-109">Example 1: Create back-end HTTP settings</span></span>
```
PS C:\>$Setting = New-AzureRmApplicationGatewayBackendHttpSettings -Name "Setting01" -Port 80 -Protocol Http -CookieBasedAffinity Disabled
```

<span data-ttu-id="7cd1c-110">Dieser Befehl erstellt HTTP-Back-End-Einstellungen mit dem Namen Setting01 auf Port 80 unter Verwendung des HTTP-Protokolls mit deaktivierter Cookie-basierter Affinität.</span><span class="sxs-lookup"><span data-stu-id="7cd1c-110">This command creates back-end HTTP settings named Setting01 on port 80, using the HTTP protocol, with cookie-based affinity disabled.</span></span>
<span data-ttu-id="7cd1c-111">Die Einstellungen werden in der $Setting-Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7cd1c-111">The settings are stored in the $Setting variable.</span></span>

## <span data-ttu-id="7cd1c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7cd1c-112">PARAMETERS</span></span>

### <span data-ttu-id="7cd1c-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="7cd1c-113">-AffinityCookieName</span></span>
<span data-ttu-id="7cd1c-114">Für das Affinitäts Cookie zu verwendender Cookie-Name</span><span class="sxs-lookup"><span data-stu-id="7cd1c-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="7cd1c-115">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="7cd1c-115">-AuthenticationCertificates</span></span>
<span data-ttu-id="7cd1c-116">Gibt Authentifizierungszertifikate für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="7cd1c-116">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="7cd1c-117">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="7cd1c-117">-ConnectionDraining</span></span>
<span data-ttu-id="7cd1c-118">Verbindungs Entleerung der HTTP-Back-End-Einstellungen-Ressource.</span><span class="sxs-lookup"><span data-stu-id="7cd1c-118">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="7cd1c-119">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="7cd1c-119">-CookieBasedAffinity</span></span>
<span data-ttu-id="7cd1c-120">Gibt an, ob die auf Cookies basierende Affinität für den Back-End-Serverpool aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7cd1c-120">Specifies whether cookie-based affinity should be enabled or disabled for the back-end server pool.</span></span>

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

### <span data-ttu-id="7cd1c-121">-Hostname</span><span class="sxs-lookup"><span data-stu-id="7cd1c-121">-HostName</span></span>
<span data-ttu-id="7cd1c-122">Legt fest, dass der Hostheader an die Back-End-Server gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="7cd1c-122">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="7cd1c-123">-Name</span><span class="sxs-lookup"><span data-stu-id="7cd1c-123">-Name</span></span>
<span data-ttu-id="7cd1c-124">Gibt den Namen der vom Cmdlet erstellten Back-End-HTTP-Einstellungen an.</span><span class="sxs-lookup"><span data-stu-id="7cd1c-124">Specifies the name of the back-end HTTP settings that this cmdlet creates.</span></span>

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

### <span data-ttu-id="7cd1c-125">-Path</span><span class="sxs-lookup"><span data-stu-id="7cd1c-125">-Path</span></span>
<span data-ttu-id="7cd1c-126">Path, der als Präfix für alle HTTP-Anforderungen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7cd1c-126">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="7cd1c-127">Wenn für diesen Parameter kein Wert angegeben wird, wird kein Pfad mit einem Präfix versehen.</span><span class="sxs-lookup"><span data-stu-id="7cd1c-127">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="7cd1c-128">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="7cd1c-128">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="7cd1c-129">Flag, wenn der Hostheader aus dem Hostnamen des Back-End-Servers ausgewählt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7cd1c-129">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="7cd1c-130">-Port</span><span class="sxs-lookup"><span data-stu-id="7cd1c-130">-Port</span></span>
<span data-ttu-id="7cd1c-131">Gibt den Port des Back-End-Server Pools an.</span><span class="sxs-lookup"><span data-stu-id="7cd1c-131">Specifies the port of the back-end server pool.</span></span>

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

### <span data-ttu-id="7cd1c-132">-Sonde</span><span class="sxs-lookup"><span data-stu-id="7cd1c-132">-Probe</span></span>
<span data-ttu-id="7cd1c-133">Gibt einen Prüfpunkt an, der dem Back-End-Serverpool zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7cd1c-133">Specifies a probe to associate with the back-end server pool.</span></span>

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

### <span data-ttu-id="7cd1c-134">-ProbeEnabled</span><span class="sxs-lookup"><span data-stu-id="7cd1c-134">-ProbeEnabled</span></span>
<span data-ttu-id="7cd1c-135">Flag, wenn Prüfpunkt aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7cd1c-135">Flag if probe should be enabled.</span></span>

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

### <span data-ttu-id="7cd1c-136">-Sonde</span><span class="sxs-lookup"><span data-stu-id="7cd1c-136">-ProbeId</span></span>
<span data-ttu-id="7cd1c-137">Gibt die ID des Prüfpunkts an, der dem Back-End-Serverpool zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7cd1c-137">Specifies the ID of the probe to associate with the back-end server pool.</span></span>

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

### <span data-ttu-id="7cd1c-138">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="7cd1c-138">-Protocol</span></span>
<span data-ttu-id="7cd1c-139">Gibt das Protokoll an, das für die Kommunikation zwischen dem Anwendungsgateway und den Back-End-Servern verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7cd1c-139">Specifies the protocol to use for communication between the application gateway and the back-end servers.</span></span>
<span data-ttu-id="7cd1c-140">Die zulässigen Werte für diesen Parameter lauten: http und HTTPS.</span><span class="sxs-lookup"><span data-stu-id="7cd1c-140">The acceptable values for this parameter are: Http and Https.</span></span>

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

### <span data-ttu-id="7cd1c-141">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="7cd1c-141">-RequestTimeout</span></span>
<span data-ttu-id="7cd1c-142">Gibt einen Anforderungstimeout Wert an.</span><span class="sxs-lookup"><span data-stu-id="7cd1c-142">Specifies a request time-out value.</span></span>

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

### <span data-ttu-id="7cd1c-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cd1c-143">-DefaultProfile</span></span>
<span data-ttu-id="7cd1c-144">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7cd1c-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cd1c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cd1c-145">CommonParameters</span></span>
<span data-ttu-id="7cd1c-146">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cd1c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cd1c-147">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cd1c-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cd1c-148">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7cd1c-148">INPUTS</span></span>

### <span data-ttu-id="7cd1c-149">System. String</span><span class="sxs-lookup"><span data-stu-id="7cd1c-149">System.String</span></span>

## <span data-ttu-id="7cd1c-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7cd1c-150">OUTPUTS</span></span>

### <span data-ttu-id="7cd1c-151">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7cd1c-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="7cd1c-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="7cd1c-152">NOTES</span></span>

## <span data-ttu-id="7cd1c-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7cd1c-153">RELATED LINKS</span></span>

[<span data-ttu-id="7cd1c-154">Add-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7cd1c-154">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="7cd1c-155">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7cd1c-155">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="7cd1c-156">Remove-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7cd1c-156">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="7cd1c-157">Satz-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7cd1c-157">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

