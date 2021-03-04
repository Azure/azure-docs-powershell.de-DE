---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 385a77c2b7b11d20b3ffb8d3728720b46c431d4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933880"
---
# <span data-ttu-id="ed0a6-101">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ed0a6-101">Add-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="ed0a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed0a6-102">SYNOPSIS</span></span>
<span data-ttu-id="ed0a6-103">Fügt einem Anwendungsgateway einen Integritätstest hinzu.</span><span class="sxs-lookup"><span data-stu-id="ed0a6-103">Adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="ed0a6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ed0a6-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed0a6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ed0a6-105">DESCRIPTION</span></span>
<span data-ttu-id="ed0a6-106">Das Add-AzApplicationGatewayProbeConfig-Cmdlet fügt einem Anwendungsgateway einen Integritätstest hinzu.</span><span class="sxs-lookup"><span data-stu-id="ed0a6-106">The Add-AzApplicationGatewayProbeConfig cmdlet adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="ed0a6-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ed0a6-107">EXAMPLES</span></span>

### <span data-ttu-id="ed0a6-108">Beispiel 1: Hinzufügen eines Integritätstests zu einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="ed0a6-108">Example 1: Add a health probe to an application gateway</span></span>
```
PS C:\>$Probe = Add-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe01" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="ed0a6-109">Dieser Befehl fügt einen Integritätstest namens Probe01 für das Anwendungsgateway mit dem Namen Gateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="ed0a6-109">This command adds a health probe named Probe01 for the application gateway named Gateway.</span></span>
<span data-ttu-id="ed0a6-110">Der Befehl legt außerdem den Schwellenwert für fehlerhafte Fehler auf 8 Wiederholungen und einen Zeitsprung nach 120 Sekunden fest.</span><span class="sxs-lookup"><span data-stu-id="ed0a6-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="ed0a6-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ed0a6-111">PARAMETERS</span></span>

### <span data-ttu-id="ed0a6-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ed0a6-112">-ApplicationGateway</span></span>
<span data-ttu-id="ed0a6-113">Gibt das Anwendungsgateway an, dem dieses Cmdlet einen Prüfpunkt hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="ed0a6-113">Specifies the application gateway to which this cmdlet adds a probe.</span></span>

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

### <span data-ttu-id="ed0a6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed0a6-114">-DefaultProfile</span></span>
<span data-ttu-id="ed0a6-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ed0a6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed0a6-116">-HostName</span><span class="sxs-lookup"><span data-stu-id="ed0a6-116">-HostName</span></span>
<span data-ttu-id="ed0a6-117">Gibt den Hostnamen an, an den dieses Cmdlet den Prüfpunkt sendet.</span><span class="sxs-lookup"><span data-stu-id="ed0a6-117">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="ed0a6-118">-Interval</span><span class="sxs-lookup"><span data-stu-id="ed0a6-118">-Interval</span></span>
<span data-ttu-id="ed0a6-119">Gibt das Sondenintervall in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="ed0a6-119">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="ed0a6-120">Dies ist das Zeitintervall zwischen zwei aufeinander folgenden Sonden.</span><span class="sxs-lookup"><span data-stu-id="ed0a6-120">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="ed0a6-121">Dieser Wert liegt zwischen 1 Sekunde und 86400 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="ed0a6-121">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="ed0a6-122">-Match</span><span class="sxs-lookup"><span data-stu-id="ed0a6-122">-Match</span></span>
<span data-ttu-id="ed0a6-123">Textkörper, der in der Integritätsantwort enthalten sein muss.</span><span class="sxs-lookup"><span data-stu-id="ed0a6-123">Body that must be contained in the health response.</span></span>
<span data-ttu-id="ed0a6-124">Standardwert ist leer</span><span class="sxs-lookup"><span data-stu-id="ed0a6-124">Default value is empty</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed0a6-125">-MinServers</span><span class="sxs-lookup"><span data-stu-id="ed0a6-125">-MinServers</span></span>
<span data-ttu-id="ed0a6-126">Mindestanzahl von Servern, die immer als fehlerfrei gekennzeichnet sind.</span><span class="sxs-lookup"><span data-stu-id="ed0a6-126">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="ed0a6-127">Standardwert ist 0</span><span class="sxs-lookup"><span data-stu-id="ed0a6-127">Default value is 0</span></span>

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

### <span data-ttu-id="ed0a6-128">-Name</span><span class="sxs-lookup"><span data-stu-id="ed0a6-128">-Name</span></span>
<span data-ttu-id="ed0a6-129">Gibt den Namen des Prüfpunkts an.</span><span class="sxs-lookup"><span data-stu-id="ed0a6-129">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="ed0a6-130">-Path</span><span class="sxs-lookup"><span data-stu-id="ed0a6-130">-Path</span></span>
<span data-ttu-id="ed0a6-131">Gibt den relativen Pfad des Prüfpunkts an.</span><span class="sxs-lookup"><span data-stu-id="ed0a6-131">Specifies the relative path of probe.</span></span>
<span data-ttu-id="ed0a6-132">Gültiger Pfad beginnt mit dem Schrägstrichzeichen (/).</span><span class="sxs-lookup"><span data-stu-id="ed0a6-132">Valid path start with the slash character (/).</span></span>
<span data-ttu-id="ed0a6-133">Der Prüfpunkt wird an \<Protocol\> :// \<host\> gesendet: \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="ed0a6-133">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="ed0a6-134">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="ed0a6-134">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="ed0a6-135">Gibt an, ob der Hostheader aus den Http-Einstellungen des Back-Ends ausgewählt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed0a6-135">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="ed0a6-136">Standardwert ist falsch</span><span class="sxs-lookup"><span data-stu-id="ed0a6-136">Default value is false</span></span>

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

### <span data-ttu-id="ed0a6-137">-Protocol</span><span class="sxs-lookup"><span data-stu-id="ed0a6-137">-Protocol</span></span>
<span data-ttu-id="ed0a6-138">Gibt das Protokoll an, das zum Senden von Prüfpunkt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ed0a6-138">Specifies the protocol used to send probe.</span></span>
<span data-ttu-id="ed0a6-139">Dieses Cmdlet unterstützt nur HTTP.</span><span class="sxs-lookup"><span data-stu-id="ed0a6-139">This cmdlet supports HTTP only.</span></span>

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

### <span data-ttu-id="ed0a6-140">-Timeout</span><span class="sxs-lookup"><span data-stu-id="ed0a6-140">-Timeout</span></span>
<span data-ttu-id="ed0a6-141">Gibt das Testtimeout in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="ed0a6-141">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="ed0a6-142">Dieses Cmdlet kennzeichnet den Prüfpunkt als fehlgeschlagen, wenn bei diesem Timeoutzeitraum keine gültige Antwort empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="ed0a6-142">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="ed0a6-143">Gültige Werte liegen zwischen 1 Sekunde und 86400 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="ed0a6-143">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="ed0a6-144">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="ed0a6-144">-UnhealthyThreshold</span></span>
<span data-ttu-id="ed0a6-145">Gibt die Anzahl der Wiederholungsversuche an.</span><span class="sxs-lookup"><span data-stu-id="ed0a6-145">Specifies the probe retry count.</span></span>
<span data-ttu-id="ed0a6-146">Der Back-End-Server ist nach dem Erreichen des Schwellenwerts für fehlerhafte Tests nach unten gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="ed0a6-146">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="ed0a6-147">Gültige Werte liegen zwischen 1 Sekunde und 20 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="ed0a6-147">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="ed0a6-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed0a6-148">CommonParameters</span></span>
<span data-ttu-id="ed0a6-149">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed0a6-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed0a6-150">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed0a6-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed0a6-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ed0a6-151">INPUTS</span></span>

### <span data-ttu-id="ed0a6-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ed0a6-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ed0a6-153">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ed0a6-153">OUTPUTS</span></span>

### <span data-ttu-id="ed0a6-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ed0a6-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ed0a6-155">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ed0a6-155">NOTES</span></span>

## <span data-ttu-id="ed0a6-156">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ed0a6-156">RELATED LINKS</span></span>

[<span data-ttu-id="ed0a6-157">Hinzufügen eines Prüfpunkts zu einem vorhandenen Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="ed0a6-157">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="ed0a6-158">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ed0a6-158">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="ed0a6-159">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ed0a6-159">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="ed0a6-160">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ed0a6-160">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="ed0a6-161">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ed0a6-161">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

