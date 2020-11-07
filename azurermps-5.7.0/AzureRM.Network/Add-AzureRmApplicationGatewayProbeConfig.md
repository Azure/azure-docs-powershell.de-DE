---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 450bb356bdd930585f9c6c69a23f3c4522a669ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663470"
---
# <span data-ttu-id="3be97-101">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3be97-101">Add-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="3be97-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3be97-102">SYNOPSIS</span></span>
<span data-ttu-id="3be97-103">Fügt ein Integritäts Prüf Punkt zu einem Anwendungs Gateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="3be97-103">Adds a health probe to an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3be97-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3be97-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3be97-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3be97-105">DESCRIPTION</span></span>
<span data-ttu-id="3be97-106">Das Add-AzureRmApplicationGatewayProbeConfig-Cmdlet fügt einen Integritäts Prüf Punkt zu einem Anwendungs Gateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="3be97-106">The Add-AzureRmApplicationGatewayProbeConfig cmdlet adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="3be97-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3be97-107">EXAMPLES</span></span>

### <span data-ttu-id="3be97-108">Beispiel 1: Hinzufügen einer Integritätsprüfung zu einem Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="3be97-108">Example 1: Add a health probe to an application gateway</span></span>
```
PS C:\>$Probe = Add-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe01" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="3be97-109">Dieser Befehl fügt einen Integritätstest mit dem Namen "Probe01" für das Application Gateway mit dem Namen Gateway hinzu.</span><span class="sxs-lookup"><span data-stu-id="3be97-109">This command adds a health probe named Probe01 for the application gateway named Gateway.</span></span>
<span data-ttu-id="3be97-110">Der Befehl legt auch die fehlerhafte Schwelle auf 8 Wiederholungen und Timeouts nach 120 Sekunden fest.</span><span class="sxs-lookup"><span data-stu-id="3be97-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="3be97-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="3be97-111">PARAMETERS</span></span>

### <span data-ttu-id="3be97-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3be97-112">-ApplicationGateway</span></span>
<span data-ttu-id="3be97-113">Gibt das Anwendungsgateway an, dem dieses Cmdlet einen Prüfpunkt hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="3be97-113">Specifies the application gateway to which this cmdlet adds a probe.</span></span>

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

### <span data-ttu-id="3be97-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3be97-114">-DefaultProfile</span></span>
<span data-ttu-id="3be97-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3be97-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3be97-116">-Hostname</span><span class="sxs-lookup"><span data-stu-id="3be97-116">-HostName</span></span>
<span data-ttu-id="3be97-117">Gibt den Hostnamen an, an den dieses Cmdlet die Sonde sendet.</span><span class="sxs-lookup"><span data-stu-id="3be97-117">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="3be97-118">-Intervall</span><span class="sxs-lookup"><span data-stu-id="3be97-118">-Interval</span></span>
<span data-ttu-id="3be97-119">Gibt das Prüf punktintervall in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="3be97-119">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="3be97-120">Dies ist das Zeitintervall zwischen zwei aufeinanderfolgenden Prüfpunkten.</span><span class="sxs-lookup"><span data-stu-id="3be97-120">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="3be97-121">Dieser Wert liegt zwischen 1 Sekunde und 86400 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="3be97-121">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="3be97-122">-Vergleich</span><span class="sxs-lookup"><span data-stu-id="3be97-122">-Match</span></span>
<span data-ttu-id="3be97-123">Body, der in der Integritäts Antwort enthalten sein muss.</span><span class="sxs-lookup"><span data-stu-id="3be97-123">Body that must be contained in the health response.</span></span>
<span data-ttu-id="3be97-124">Der Standardwert ist leer</span><span class="sxs-lookup"><span data-stu-id="3be97-124">Default value is empty</span></span>

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

### <span data-ttu-id="3be97-125">-MinServers</span><span class="sxs-lookup"><span data-stu-id="3be97-125">-MinServers</span></span>
<span data-ttu-id="3be97-126">Minimale Anzahl von Servern, die immer als "fehlerfrei" gekennzeichnet sind.</span><span class="sxs-lookup"><span data-stu-id="3be97-126">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="3be97-127">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="3be97-127">Default value is 0</span></span>

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

### <span data-ttu-id="3be97-128">-Name</span><span class="sxs-lookup"><span data-stu-id="3be97-128">-Name</span></span>
<span data-ttu-id="3be97-129">Gibt den Namen des Prüfpunkts an.</span><span class="sxs-lookup"><span data-stu-id="3be97-129">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="3be97-130">-Path</span><span class="sxs-lookup"><span data-stu-id="3be97-130">-Path</span></span>
<span data-ttu-id="3be97-131">Gibt den relativen Pfad des Prüfpunkts an.</span><span class="sxs-lookup"><span data-stu-id="3be97-131">Specifies the relative path of probe.</span></span>
<span data-ttu-id="3be97-132">Gültiger Pfad beginnt mit dem Schrägstrich (/).</span><span class="sxs-lookup"><span data-stu-id="3be97-132">Valid path start with the slash character (/).</span></span>
<span data-ttu-id="3be97-133">Die Sonde wird an \<Protocol\> :// \<host\> : gesendet \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="3be97-133">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="3be97-134">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="3be97-134">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="3be97-135">Gibt an, ob der Hostheader über die HTTP-Back-End-Einstellungen ausgewählt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3be97-135">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="3be97-136">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="3be97-136">Default value is false</span></span>

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

### <span data-ttu-id="3be97-137">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="3be97-137">-Protocol</span></span>
<span data-ttu-id="3be97-138">Gibt das zum Senden der Sonde verwendete Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="3be97-138">Specifies the protocol used to send probe.</span></span>
<span data-ttu-id="3be97-139">Dieses Cmdlet unterstützt nur http.</span><span class="sxs-lookup"><span data-stu-id="3be97-139">This cmdlet supports HTTP only.</span></span>

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

### <span data-ttu-id="3be97-140">-Timeout</span><span class="sxs-lookup"><span data-stu-id="3be97-140">-Timeout</span></span>
<span data-ttu-id="3be97-141">Gibt das Prüfpunkt-Timeout in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="3be97-141">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="3be97-142">Dieses Cmdlet kennzeichnet die Prüfspitze als fehlerhaft, wenn bei diesem Timeoutzeitraum keine gültige Antwort empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="3be97-142">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="3be97-143">Gültige Werte liegen zwischen 1 Sekunde und 86400 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="3be97-143">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="3be97-144">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="3be97-144">-UnhealthyThreshold</span></span>
<span data-ttu-id="3be97-145">Gibt die Anzahl der Prüf Punkt Wiederholungen an.</span><span class="sxs-lookup"><span data-stu-id="3be97-145">Specifies the probe retry count.</span></span>
<span data-ttu-id="3be97-146">Der Back-End-Server wird markiert, nachdem der Fehlerzähler für aufeinanderfolgende Prüfpunkte den ungesunden Schwellenwert erreicht hat.</span><span class="sxs-lookup"><span data-stu-id="3be97-146">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="3be97-147">Gültige Werte liegen zwischen 1 Sekunde und 20 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="3be97-147">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="3be97-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3be97-148">CommonParameters</span></span>
<span data-ttu-id="3be97-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3be97-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3be97-150">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3be97-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3be97-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3be97-151">INPUTS</span></span>

### <span data-ttu-id="3be97-152">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3be97-152">PSApplicationGateway</span></span>
<span data-ttu-id="3be97-153">Der Parameter "ApplicationGateway" akzeptiert den Wert vom Typ "PSApplicationGateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="3be97-153">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="3be97-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3be97-154">OUTPUTS</span></span>

### <span data-ttu-id="3be97-155">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3be97-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3be97-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="3be97-156">NOTES</span></span>

## <span data-ttu-id="3be97-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3be97-157">RELATED LINKS</span></span>

[<span data-ttu-id="3be97-158">Hinzufügen einer Sonde zu einem vorhandenen Anwendungsgateway</span><span class="sxs-lookup"><span data-stu-id="3be97-158">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="3be97-159">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3be97-159">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="3be97-160">Neu – AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3be97-160">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="3be97-161">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3be97-161">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="3be97-162">Satz-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="3be97-162">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

