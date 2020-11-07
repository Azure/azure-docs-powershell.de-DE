---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayprobeconfig
schema: 2.0.0
ms.openlocfilehash: 7fb8a30986c31659b49a08b261062e150ebe7e09
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848107"
---
# <span data-ttu-id="3d49e-101">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3d49e-101">Set-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="3d49e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3d49e-102">SYNOPSIS</span></span>
<span data-ttu-id="3d49e-103">Legt die Konfiguration des Integritäts Prüfpunkts für ein vorhandenes Anwendungs Gateway fest.</span><span class="sxs-lookup"><span data-stu-id="3d49e-103">Sets the health probe configuration on an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d49e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d49e-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3d49e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3d49e-105">DESCRIPTION</span></span>
<span data-ttu-id="3d49e-106">Das Set-AzureRmApplicationGatewayProbeConfig-Cmdlet legt die Konfiguration des Integritäts Prüfpunkts für ein vorhandenes Anwendungs Gateway fest.</span><span class="sxs-lookup"><span data-stu-id="3d49e-106">The Set-AzureRmApplicationGatewayProbeConfig cmdlet sets the health probe configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="3d49e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3d49e-107">EXAMPLES</span></span>

### <span data-ttu-id="3d49e-108">Beispiel 1: Einrichten der Konfiguration für einen Integritäts Prüf Punkt auf einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="3d49e-108">Example 1: Set the configuration for a health probe on an application gateway</span></span>
```
PS C:\>Set-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe05" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="3d49e-109">Mit diesem Befehl wird die Konfiguration für einen Integritäts Prüf Punkt mit dem Namen "Probe05" für das Application Gateway mit dem Namen Gateway festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3d49e-109">This command sets the configuration for a health probe named Probe05 for the application gateway named Gateway.</span></span>
<span data-ttu-id="3d49e-110">Der Befehl legt auch die fehlerhafte Schwelle auf 8 Wiederholungen und Timeouts nach 120 Sekunden fest.</span><span class="sxs-lookup"><span data-stu-id="3d49e-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="3d49e-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d49e-111">PARAMETERS</span></span>

### <span data-ttu-id="3d49e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3d49e-112">-ApplicationGateway</span></span>
<span data-ttu-id="3d49e-113">Gibt das Anwendungsgateway an, an das dieses Cmdlet eine Sonde sendet.</span><span class="sxs-lookup"><span data-stu-id="3d49e-113">Specifies the application gateway to which this cmdlet sends a probe.</span></span>

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

### <span data-ttu-id="3d49e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d49e-114">-DefaultProfile</span></span>
<span data-ttu-id="3d49e-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3d49e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d49e-116">-Hostname</span><span class="sxs-lookup"><span data-stu-id="3d49e-116">-HostName</span></span>
<span data-ttu-id="3d49e-117">Gibt den Hostnamen an, an den dieses Cmdlet die Sonde sendet.</span><span class="sxs-lookup"><span data-stu-id="3d49e-117">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="3d49e-118">-Intervall</span><span class="sxs-lookup"><span data-stu-id="3d49e-118">-Interval</span></span>
<span data-ttu-id="3d49e-119">Gibt das Prüf punktintervall in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="3d49e-119">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="3d49e-120">Dies ist das Zeitintervall zwischen zwei aufeinanderfolgenden Prüfpunkten.</span><span class="sxs-lookup"><span data-stu-id="3d49e-120">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="3d49e-121">Dieser Wert liegt zwischen 1 Sekunde und 86400 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="3d49e-121">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="3d49e-122">-Vergleich</span><span class="sxs-lookup"><span data-stu-id="3d49e-122">-Match</span></span>
<span data-ttu-id="3d49e-123">Body, der in der Integritäts Antwort enthalten sein muss.</span><span class="sxs-lookup"><span data-stu-id="3d49e-123">Body that must be contained in the health response.</span></span>
<span data-ttu-id="3d49e-124">Der Standardwert ist leer</span><span class="sxs-lookup"><span data-stu-id="3d49e-124">Default value is empty</span></span>

```yaml
Type: PSApplicationGatewayProbeHealthResponseMatch
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d49e-125">-MinServers</span><span class="sxs-lookup"><span data-stu-id="3d49e-125">-MinServers</span></span>
<span data-ttu-id="3d49e-126">Minimale Anzahl von Servern, die immer als "fehlerfrei" gekennzeichnet sind.</span><span class="sxs-lookup"><span data-stu-id="3d49e-126">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="3d49e-127">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="3d49e-127">Default value is 0</span></span>

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

### <span data-ttu-id="3d49e-128">-Name</span><span class="sxs-lookup"><span data-stu-id="3d49e-128">-Name</span></span>
<span data-ttu-id="3d49e-129">Gibt den Namen des Prüfpunkts an.</span><span class="sxs-lookup"><span data-stu-id="3d49e-129">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="3d49e-130">-Path</span><span class="sxs-lookup"><span data-stu-id="3d49e-130">-Path</span></span>
<span data-ttu-id="3d49e-131">Gibt den relativen Pfad des Prüfpunkts an.</span><span class="sxs-lookup"><span data-stu-id="3d49e-131">Specifies the relative path of probe.</span></span>
<span data-ttu-id="3d49e-132">Gültige Pfade beginnen mit dem Schrägstrich (/).</span><span class="sxs-lookup"><span data-stu-id="3d49e-132">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="3d49e-133">Die Sonde wird an \<Protocol\> :// \<host\> : gesendet \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="3d49e-133">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="3d49e-134">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="3d49e-134">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="3d49e-135">Gibt an, ob der Hostheader über die HTTP-Back-End-Einstellungen ausgewählt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3d49e-135">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="3d49e-136">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="3d49e-136">Default value is false</span></span>

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

### <span data-ttu-id="3d49e-137">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="3d49e-137">-Protocol</span></span>
<span data-ttu-id="3d49e-138">Gibt das zum Senden der Sonde verwendete Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="3d49e-138">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="3d49e-139">-Timeout</span><span class="sxs-lookup"><span data-stu-id="3d49e-139">-Timeout</span></span>
<span data-ttu-id="3d49e-140">Gibt das Prüfpunkt-Timeout in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="3d49e-140">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="3d49e-141">Dieses Cmdlet kennzeichnet die Prüfspitze als fehlerhaft, wenn bei diesem Timeoutzeitraum keine gültige Antwort empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="3d49e-141">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="3d49e-142">Gültige Werte liegen zwischen 1 Sekunde und 86400 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="3d49e-142">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="3d49e-143">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="3d49e-143">-UnhealthyThreshold</span></span>
<span data-ttu-id="3d49e-144">Gibt die Anzahl der Prüf Punkt Wiederholungen an.</span><span class="sxs-lookup"><span data-stu-id="3d49e-144">Specifies the probe retry count.</span></span>
<span data-ttu-id="3d49e-145">Der Back-End-Server wird markiert, nachdem der Fehlerzähler für aufeinanderfolgende Prüfpunkte den ungesunden Schwellenwert erreicht hat.</span><span class="sxs-lookup"><span data-stu-id="3d49e-145">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="3d49e-146">Gültige Werte liegen zwischen 1 Sekunde und 20 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="3d49e-146">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="3d49e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d49e-147">CommonParameters</span></span>
<span data-ttu-id="3d49e-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d49e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d49e-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d49e-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d49e-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3d49e-150">INPUTS</span></span>

### <span data-ttu-id="3d49e-151">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3d49e-151">PSApplicationGateway</span></span>
<span data-ttu-id="3d49e-152">Der Parameter "ApplicationGateway" akzeptiert den Wert vom Typ "PSApplicationGateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="3d49e-152">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="3d49e-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3d49e-153">OUTPUTS</span></span>

### <span data-ttu-id="3d49e-154">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3d49e-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3d49e-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="3d49e-155">NOTES</span></span>

## <span data-ttu-id="3d49e-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3d49e-156">RELATED LINKS</span></span>

[<span data-ttu-id="3d49e-157">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3d49e-157">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="3d49e-158">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3d49e-158">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="3d49e-159">Neu – AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3d49e-159">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="3d49e-160">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3d49e-160">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

