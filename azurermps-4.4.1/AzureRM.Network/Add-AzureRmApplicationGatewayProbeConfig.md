---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 169a63248ebc499f577a635821131e0153e64433
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501769"
---
# <span data-ttu-id="775c0-101">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="775c0-101">Add-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="775c0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="775c0-102">SYNOPSIS</span></span>
<span data-ttu-id="775c0-103">Fügt ein Integritäts Prüf Punkt zu einem Anwendungs Gateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="775c0-103">Adds a health probe to an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="775c0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="775c0-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="775c0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="775c0-105">DESCRIPTION</span></span>
<span data-ttu-id="775c0-106">Das Add-AzureRmApplicationGatewayProbeConfig-Cmdlet fügt einen Integritäts Prüf Punkt zu einem Anwendungs Gateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="775c0-106">The Add-AzureRmApplicationGatewayProbeConfig cmdlet adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="775c0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="775c0-107">EXAMPLES</span></span>

### <span data-ttu-id="775c0-108">Beispiel 1: Hinzufügen einer Integritätsprüfung zu einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="775c0-108">Example 1: Add a health probe to an application gateway</span></span>
```
PS C:\>$Probe = Add-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe01" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="775c0-109">Dieser Befehl fügt einen Integritätstest mit dem Namen "Probe01" für das Application Gateway mit dem Namen Gateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="775c0-109">This command adds a health probe named Probe01 for the application gateway named Gateway.</span></span>
<span data-ttu-id="775c0-110">Der Befehl legt auch die fehlerhafte Schwelle auf 8 Wiederholungen und Timeouts nach 120 Sekunden fest.</span><span class="sxs-lookup"><span data-stu-id="775c0-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="775c0-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="775c0-111">PARAMETERS</span></span>

### <span data-ttu-id="775c0-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="775c0-112">-ApplicationGateway</span></span>
<span data-ttu-id="775c0-113">Gibt das Anwendungsgateway an, dem dieses Cmdlet einen Prüfpunkt hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="775c0-113">Specifies the application gateway to which this cmdlet adds a probe.</span></span>

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

### <span data-ttu-id="775c0-114">-Hostname</span><span class="sxs-lookup"><span data-stu-id="775c0-114">-HostName</span></span>
<span data-ttu-id="775c0-115">Gibt den Hostnamen an, an den dieses Cmdlet die Sonde sendet.</span><span class="sxs-lookup"><span data-stu-id="775c0-115">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="775c0-116">-Intervall</span><span class="sxs-lookup"><span data-stu-id="775c0-116">-Interval</span></span>
<span data-ttu-id="775c0-117">Gibt das Prüf punktintervall in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="775c0-117">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="775c0-118">Dies ist das Zeitintervall zwischen zwei aufeinanderfolgenden Prüfpunkten.</span><span class="sxs-lookup"><span data-stu-id="775c0-118">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="775c0-119">Dieser Wert liegt zwischen 1 Sekunde und 86400 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="775c0-119">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="775c0-120">-Vergleich</span><span class="sxs-lookup"><span data-stu-id="775c0-120">-Match</span></span>
<span data-ttu-id="775c0-121">Body, der in der Integritäts Antwort enthalten sein muss.</span><span class="sxs-lookup"><span data-stu-id="775c0-121">Body that must be contained in the health response.</span></span>
<span data-ttu-id="775c0-122">Der Standardwert ist leer</span><span class="sxs-lookup"><span data-stu-id="775c0-122">Default value is empty</span></span>

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

### <span data-ttu-id="775c0-123">-MinServers</span><span class="sxs-lookup"><span data-stu-id="775c0-123">-MinServers</span></span>
<span data-ttu-id="775c0-124">Minimale Anzahl von Servern, die immer als "fehlerfrei" gekennzeichnet sind.</span><span class="sxs-lookup"><span data-stu-id="775c0-124">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="775c0-125">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="775c0-125">Default value is 0</span></span>

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

### <span data-ttu-id="775c0-126">-Name</span><span class="sxs-lookup"><span data-stu-id="775c0-126">-Name</span></span>
<span data-ttu-id="775c0-127">Gibt den Namen des Prüfpunkts an.</span><span class="sxs-lookup"><span data-stu-id="775c0-127">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="775c0-128">-Path</span><span class="sxs-lookup"><span data-stu-id="775c0-128">-Path</span></span>
<span data-ttu-id="775c0-129">Gibt den relativen Pfad des Prüfpunkts an.</span><span class="sxs-lookup"><span data-stu-id="775c0-129">Specifies the relative path of probe.</span></span>
<span data-ttu-id="775c0-130">Gültiger Pfad beginnt mit dem Schrägstrich (/).</span><span class="sxs-lookup"><span data-stu-id="775c0-130">Valid path start with the slash character (/).</span></span>
<span data-ttu-id="775c0-131">Die Sonde wird an \<Protocol\> :// \<host\> : gesendet \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="775c0-131">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="775c0-132">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="775c0-132">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="775c0-133">Gibt an, ob der Hostheader über die HTTP-Back-End-Einstellungen ausgewählt werden soll.</span><span class="sxs-lookup"><span data-stu-id="775c0-133">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="775c0-134">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="775c0-134">Default value is false</span></span>

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

### <span data-ttu-id="775c0-135">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="775c0-135">-Protocol</span></span>
<span data-ttu-id="775c0-136">Gibt das zum Senden der Sonde verwendete Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="775c0-136">Specifies the protocol used to send probe.</span></span>
<span data-ttu-id="775c0-137">Dieses Cmdlet unterstützt nur http.</span><span class="sxs-lookup"><span data-stu-id="775c0-137">This cmdlet supports HTTP only.</span></span>

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

### <span data-ttu-id="775c0-138">-Timeout</span><span class="sxs-lookup"><span data-stu-id="775c0-138">-Timeout</span></span>
<span data-ttu-id="775c0-139">Gibt das Prüfpunkt-Timeout in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="775c0-139">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="775c0-140">Dieses Cmdlet kennzeichnet die Prüfspitze als fehlerhaft, wenn bei diesem Timeoutzeitraum keine gültige Antwort empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="775c0-140">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="775c0-141">Gültige Werte liegen zwischen 1 Sekunde und 86400 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="775c0-141">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="775c0-142">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="775c0-142">-UnhealthyThreshold</span></span>
<span data-ttu-id="775c0-143">Gibt die Anzahl der Prüf Punkt Wiederholungen an.</span><span class="sxs-lookup"><span data-stu-id="775c0-143">Specifies the probe retry count.</span></span>
<span data-ttu-id="775c0-144">Der Back-End-Server wird markiert, nachdem der Fehlerzähler für aufeinanderfolgende Prüfpunkte den ungesunden Schwellenwert erreicht hat.</span><span class="sxs-lookup"><span data-stu-id="775c0-144">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="775c0-145">Gültige Werte liegen zwischen 1 Sekunde und 20 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="775c0-145">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="775c0-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="775c0-146">-DefaultProfile</span></span>
<span data-ttu-id="775c0-147">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="775c0-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="775c0-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="775c0-148">CommonParameters</span></span>
<span data-ttu-id="775c0-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="775c0-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="775c0-150">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="775c0-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="775c0-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="775c0-151">INPUTS</span></span>

### <span data-ttu-id="775c0-152">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="775c0-152">PSApplicationGateway</span></span>
<span data-ttu-id="775c0-153">Der Parameter "ApplicationGateway" akzeptiert den Wert vom Typ "PSApplicationGateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="775c0-153">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="775c0-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="775c0-154">OUTPUTS</span></span>

### <span data-ttu-id="775c0-155">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="775c0-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="775c0-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="775c0-156">NOTES</span></span>

## <span data-ttu-id="775c0-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="775c0-157">RELATED LINKS</span></span>

[<span data-ttu-id="775c0-158">Hinzufügen einer Sonde zu einem vorhandenen Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="775c0-158">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="775c0-159">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="775c0-159">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="775c0-160">Neu – AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="775c0-160">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="775c0-161">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="775c0-161">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="775c0-162">Satz-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="775c0-162">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

