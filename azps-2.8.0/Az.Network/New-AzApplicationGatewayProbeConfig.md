---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 61afe67e06316dc94948be00e4778394594468cd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821643"
---
# <span data-ttu-id="f14d3-101">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f14d3-101">New-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="f14d3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f14d3-102">SYNOPSIS</span></span>
<span data-ttu-id="f14d3-103">Erstellt eine Integritätsprüfung.</span><span class="sxs-lookup"><span data-stu-id="f14d3-103">Creates a health probe.</span></span>

## <span data-ttu-id="f14d3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f14d3-104">SYNTAX</span></span>

```
New-AzApplicationGatewayProbeConfig -Name <String> -Protocol <String> [-HostName <String>] -Path <String>
 -Interval <Int32> -Timeout <Int32> -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings]
 [-MinServers <Int32>] [-Match <PSApplicationGatewayProbeHealthResponseMatch>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>] [-Port <Int32>]
```

## <span data-ttu-id="f14d3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f14d3-105">DESCRIPTION</span></span>
<span data-ttu-id="f14d3-106">Das New-AzApplicationGatewayProbeConfig-Cmdlet erstellt einen Integritäts Prüf Punkt.</span><span class="sxs-lookup"><span data-stu-id="f14d3-106">The New-AzApplicationGatewayProbeConfig cmdlet creates a health probe.</span></span>

## <span data-ttu-id="f14d3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f14d3-107">EXAMPLES</span></span>

### <span data-ttu-id="f14d3-108">Beispiel1: Erstellen eines Integritäts Prüfpunkts</span><span class="sxs-lookup"><span data-stu-id="f14d3-108">Example1: Create a health probe</span></span>
```
PS C:\>New-AzApplicationGatewayProbeConfig -Name "Probe03" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="f14d3-109">Dieser Befehl erstellt einen Integritätstest mit dem Namen "Probe03" mit HTTP-Protokoll, einem Intervall von 30 Sekunden, einem Timeout von 120 Sekunden und einem fehlerhaften Schwellenwert von 8 Wiederholungen.</span><span class="sxs-lookup"><span data-stu-id="f14d3-109">This command creates a health probe named Probe03, with HTTP protocol, a 30 second interval, timeout of 120 seconds, and an unhealthy threshold of 8 retries.</span></span>

## <span data-ttu-id="f14d3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f14d3-110">PARAMETERS</span></span>

### <span data-ttu-id="f14d3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f14d3-111">-DefaultProfile</span></span>
<span data-ttu-id="f14d3-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f14d3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f14d3-113">-Hostname</span><span class="sxs-lookup"><span data-stu-id="f14d3-113">-HostName</span></span>
<span data-ttu-id="f14d3-114">Gibt den Hostnamen an, den dieses Cmdlet an die Sonde sendet.</span><span class="sxs-lookup"><span data-stu-id="f14d3-114">Specifies the host name that this cmdlet sends the probe.</span></span>

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

### <span data-ttu-id="f14d3-115">-Intervall</span><span class="sxs-lookup"><span data-stu-id="f14d3-115">-Interval</span></span>
<span data-ttu-id="f14d3-116">Gibt das Prüf punktintervall in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="f14d3-116">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="f14d3-117">Dies ist das Zeitintervall zwischen zwei aufeinanderfolgenden Prüfpunkten.</span><span class="sxs-lookup"><span data-stu-id="f14d3-117">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="f14d3-118">Dieser Wert liegt zwischen 1 Sekunde und 86400 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="f14d3-118">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="f14d3-119">-Vergleich</span><span class="sxs-lookup"><span data-stu-id="f14d3-119">-Match</span></span>
<span data-ttu-id="f14d3-120">Body, der in der Integritäts Antwort enthalten sein muss.</span><span class="sxs-lookup"><span data-stu-id="f14d3-120">Body that must be contained in the health response.</span></span>
<span data-ttu-id="f14d3-121">Der Standardwert ist leer</span><span class="sxs-lookup"><span data-stu-id="f14d3-121">Default value is empty</span></span>

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

### <span data-ttu-id="f14d3-122">-MinServers</span><span class="sxs-lookup"><span data-stu-id="f14d3-122">-MinServers</span></span>
<span data-ttu-id="f14d3-123">Minimale Anzahl von Servern, die immer als "fehlerfrei" gekennzeichnet sind.</span><span class="sxs-lookup"><span data-stu-id="f14d3-123">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="f14d3-124">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="f14d3-124">Default value is 0</span></span>

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

### <span data-ttu-id="f14d3-125">-Name</span><span class="sxs-lookup"><span data-stu-id="f14d3-125">-Name</span></span>
<span data-ttu-id="f14d3-126">Gibt den Namen des Prüfpunkts an.</span><span class="sxs-lookup"><span data-stu-id="f14d3-126">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="f14d3-127">-Path</span><span class="sxs-lookup"><span data-stu-id="f14d3-127">-Path</span></span>
<span data-ttu-id="f14d3-128">Gibt den relativen Pfad des Prüfpunkts an.</span><span class="sxs-lookup"><span data-stu-id="f14d3-128">Specifies the relative path of probe.</span></span>
<span data-ttu-id="f14d3-129">Gültige Pfade beginnen mit dem Schrägstrich (/).</span><span class="sxs-lookup"><span data-stu-id="f14d3-129">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="f14d3-130">Die Sonde wird an das \< Protokoll \> :// \< Host \> : \< Port \> \< path gesendet \> .</span><span class="sxs-lookup"><span data-stu-id="f14d3-130">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="f14d3-131">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f14d3-131">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="f14d3-132">Gibt an, ob der Hostheader über die HTTP-Back-End-Einstellungen ausgewählt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f14d3-132">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="f14d3-133">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="f14d3-133">Default value is false</span></span>

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

### <span data-ttu-id="f14d3-134">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="f14d3-134">-Protocol</span></span>
<span data-ttu-id="f14d3-135">Gibt das zum Senden der Sonde verwendete Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="f14d3-135">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="f14d3-136">-Timeout</span><span class="sxs-lookup"><span data-stu-id="f14d3-136">-Timeout</span></span>
<span data-ttu-id="f14d3-137">Gibt das Prüfpunkt-Timeout in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="f14d3-137">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="f14d3-138">Dieses Cmdlet kennzeichnet die Prüfspitze als fehlerhaft, wenn bei diesem Timeoutzeitraum keine gültige Antwort empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="f14d3-138">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="f14d3-139">Gültige Werte liegen zwischen 1 Sekunde und 86400 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="f14d3-139">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="f14d3-140">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="f14d3-140">-UnhealthyThreshold</span></span>
<span data-ttu-id="f14d3-141">Gibt die Anzahl der Prüf Punkt Wiederholungen an.</span><span class="sxs-lookup"><span data-stu-id="f14d3-141">Specifies the probe retry count.</span></span>
<span data-ttu-id="f14d3-142">Der Back-End-Server wird markiert, nachdem der Fehlerzähler für aufeinanderfolgende Prüfpunkte den ungesunden Schwellenwert erreicht hat.</span><span class="sxs-lookup"><span data-stu-id="f14d3-142">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="f14d3-143">Gültige Werte liegen zwischen 1 Sekunde und 20 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="f14d3-143">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="f14d3-144">-Port</span><span class="sxs-lookup"><span data-stu-id="f14d3-144">-Port</span></span>
<span data-ttu-id="f14d3-145">Gibt den Port an, der für die Suche nach Back-End-Servern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f14d3-145">Specifies the port used for probing backend servers.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe

## NOTES

## RELATED LINKS

[Create custom probe for Application Gateway using PowerShell for Azure Resource Manager](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#)

[Add-AzApplicationGatewayProbeConfig](./Add-AzApplicationGatewayProbeConfig.md)

[Get-AzApplicationGatewayProbeConfig](./Get-AzApplicationGatewayProbeConfig.md)

[Remove-AzApplicationGatewayProbeConfig](./Remove-AzApplicationGatewayProbeConfig.md)

[Set-AzApplicationGatewayProbeConfig](./Set-AzApplicationGatewayProbeConfig.md)

