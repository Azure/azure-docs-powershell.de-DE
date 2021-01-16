---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: cea6f92ba15e43d5977af03dfee1054240f5ecad
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468255"
---
# <span data-ttu-id="22566-101">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="22566-101">Add-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="22566-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22566-102">SYNOPSIS</span></span>
<span data-ttu-id="22566-103">Fügt einem Anwendungsgateway eine Integritätsprobe hinzu.</span><span class="sxs-lookup"><span data-stu-id="22566-103">Adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="22566-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="22566-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="22566-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="22566-105">DESCRIPTION</span></span>
<span data-ttu-id="22566-106">Das Add-AzApplicationGatewayProbeConfig cmdlet fügt einem Anwendungsgateway eine Integritätsinteprobe hinzu.</span><span class="sxs-lookup"><span data-stu-id="22566-106">The Add-AzApplicationGatewayProbeConfig cmdlet adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="22566-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="22566-107">EXAMPLES</span></span>

### <span data-ttu-id="22566-108">Beispiel 1: Hinzufügen einer Integritätsprobe zu einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="22566-108">Example 1: Add a health probe to an application gateway</span></span>
```
PS C:\>$Probe = Add-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe01" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="22566-109">Mit diesem Befehl wird eine Integritätsprobe namens "Probe01" für das Anwendungsgateway namens "Gateway" hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="22566-109">This command adds a health probe named Probe01 for the application gateway named Gateway.</span></span>
<span data-ttu-id="22566-110">Der Befehl legt außerdem den fehlerhaften Schwellenwert auf 8 Wiederholungen und ein Zeit out nach 120 Sekunden fest.</span><span class="sxs-lookup"><span data-stu-id="22566-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="22566-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22566-111">PARAMETERS</span></span>

### <span data-ttu-id="22566-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="22566-112">-ApplicationGateway</span></span>
<span data-ttu-id="22566-113">Gibt das Anwendungsgateway an, dem dieses Cmdlet eine Sonde hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="22566-113">Specifies the application gateway to which this cmdlet adds a probe.</span></span>

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

### <span data-ttu-id="22566-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22566-114">-DefaultProfile</span></span>
<span data-ttu-id="22566-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="22566-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22566-116">-HostName</span><span class="sxs-lookup"><span data-stu-id="22566-116">-HostName</span></span>
<span data-ttu-id="22566-117">Gibt den Hostnamen an, an den das Cmdlet die Sonde sendet.</span><span class="sxs-lookup"><span data-stu-id="22566-117">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="22566-118">-Interval</span><span class="sxs-lookup"><span data-stu-id="22566-118">-Interval</span></span>
<span data-ttu-id="22566-119">Gibt das Testintervall in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="22566-119">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="22566-120">Dies ist das Zeitintervall zwischen zwei aufeinander folgenden Sonden.</span><span class="sxs-lookup"><span data-stu-id="22566-120">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="22566-121">Dieser Wert liegt zwischen einer Sekunde und 86400 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="22566-121">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="22566-122">-Match</span><span class="sxs-lookup"><span data-stu-id="22566-122">-Match</span></span>
<span data-ttu-id="22566-123">Text, der in der Gesundheitsantwort enthalten sein muss.</span><span class="sxs-lookup"><span data-stu-id="22566-123">Body that must be contained in the health response.</span></span>
<span data-ttu-id="22566-124">Der Standardwert ist leer.</span><span class="sxs-lookup"><span data-stu-id="22566-124">Default value is empty</span></span>

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

### <span data-ttu-id="22566-125">-MinServers</span><span class="sxs-lookup"><span data-stu-id="22566-125">-MinServers</span></span>
<span data-ttu-id="22566-126">Mindestanzahl von Servern, die immer als fehlerfrei gekennzeichnet sind.</span><span class="sxs-lookup"><span data-stu-id="22566-126">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="22566-127">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="22566-127">Default value is 0</span></span>

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

### <span data-ttu-id="22566-128">-Name</span><span class="sxs-lookup"><span data-stu-id="22566-128">-Name</span></span>
<span data-ttu-id="22566-129">Gibt den Namen der Sonde an.</span><span class="sxs-lookup"><span data-stu-id="22566-129">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="22566-130">-Path</span><span class="sxs-lookup"><span data-stu-id="22566-130">-Path</span></span>
<span data-ttu-id="22566-131">Gibt den relativen Pfad der Sonde an.</span><span class="sxs-lookup"><span data-stu-id="22566-131">Specifies the relative path of probe.</span></span>
<span data-ttu-id="22566-132">Gültiger Pfad beginnt mit dem Schrägstrich (/).</span><span class="sxs-lookup"><span data-stu-id="22566-132">Valid path start with the slash character (/).</span></span>
<span data-ttu-id="22566-133">Die Sonde wird an \<Protocol\> \<host\> ://: \<port\> \<path\> gesendet.</span><span class="sxs-lookup"><span data-stu-id="22566-133">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="22566-134">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="22566-134">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="22566-135">Gibt an, ob der Hostheader aus den Http-Back-End-Einstellungen ausgewählt werden soll.</span><span class="sxs-lookup"><span data-stu-id="22566-135">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="22566-136">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="22566-136">Default value is false</span></span>

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

### <span data-ttu-id="22566-137">-Protocol</span><span class="sxs-lookup"><span data-stu-id="22566-137">-Protocol</span></span>
<span data-ttu-id="22566-138">Gibt das Protokoll an, das zum Senden der Sonde verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="22566-138">Specifies the protocol used to send probe.</span></span>
<span data-ttu-id="22566-139">Dieses Cmdlet unterstützt nur HTTP.</span><span class="sxs-lookup"><span data-stu-id="22566-139">This cmdlet supports HTTP only.</span></span>

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

### <span data-ttu-id="22566-140">-Timeout</span><span class="sxs-lookup"><span data-stu-id="22566-140">-Timeout</span></span>
<span data-ttu-id="22566-141">Gibt das Timeout für die Sonden in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="22566-141">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="22566-142">Mit diesem Cmdlet wird die Sonde als fehlgeschlagen markiert, wenn nach diesem Timeoutzeitraum keine gültige Antwort empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="22566-142">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="22566-143">Gültige Werte liegen zwischen einer Sekunde und 86400 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="22566-143">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="22566-144">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="22566-144">-UnhealthyThreshold</span></span>
<span data-ttu-id="22566-145">Gibt die Anzahl der Wiederholungen an.</span><span class="sxs-lookup"><span data-stu-id="22566-145">Specifies the probe retry count.</span></span>
<span data-ttu-id="22566-146">Der Back-End-Server wird nach dem Zählen aufeinanderfolgender Sondenfehler als fehlerhaft markiert.</span><span class="sxs-lookup"><span data-stu-id="22566-146">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="22566-147">Gültige Werte liegen zwischen einer Sekunde und 20 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="22566-147">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="22566-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22566-148">CommonParameters</span></span>
<span data-ttu-id="22566-149">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22566-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22566-150">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22566-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22566-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="22566-151">INPUTS</span></span>

### <span data-ttu-id="22566-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="22566-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="22566-153">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="22566-153">OUTPUTS</span></span>

### <span data-ttu-id="22566-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="22566-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="22566-155">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="22566-155">NOTES</span></span>

## <span data-ttu-id="22566-156">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="22566-156">RELATED LINKS</span></span>

[<span data-ttu-id="22566-157">Hinzufügen einer Probe zu einem vorhandenen Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="22566-157">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="22566-158">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="22566-158">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="22566-159">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="22566-159">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="22566-160">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="22566-160">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="22566-161">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="22566-161">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

