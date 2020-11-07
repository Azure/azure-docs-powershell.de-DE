---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 538020fa9ef55eedfdf7b181fca16f9499f46682
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663365"
---
# <span data-ttu-id="668f9-101">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="668f9-101">New-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="668f9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="668f9-102">SYNOPSIS</span></span>
<span data-ttu-id="668f9-103">Erstellt eine Integritätsprüfung.</span><span class="sxs-lookup"><span data-stu-id="668f9-103">Creates a health probe.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="668f9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="668f9-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayProbeConfig -Name <String> -Protocol <String> [-HostName <String>] -Path <String>
 -Interval <Int32> -Timeout <Int32> -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings]
 [-MinServers <Int32>] [-Match <PSApplicationGatewayProbeHealthResponseMatch>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="668f9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="668f9-105">DESCRIPTION</span></span>
<span data-ttu-id="668f9-106">Das New-AzureRmApplicationGatewayProbeConfig-Cmdlet erstellt einen Integritäts Prüf Punkt.</span><span class="sxs-lookup"><span data-stu-id="668f9-106">The New-AzureRmApplicationGatewayProbeConfig cmdlet creates a health probe.</span></span>

## <span data-ttu-id="668f9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="668f9-107">EXAMPLES</span></span>

### <span data-ttu-id="668f9-108">Beispiel1: Erstellen eines Integritäts Prüfpunkts</span><span class="sxs-lookup"><span data-stu-id="668f9-108">Example1: Create a health probe</span></span>
```
PS C:\>New-AzureRmApplicationGatewayProbeConfig -Name "Probe03" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="668f9-109">Dieser Befehl erstellt einen Integritätstest mit dem Namen "Probe03" mit HTTP-Protokoll, einem Intervall von 30 Sekunden, einem Timeout von 120 Sekunden und einem fehlerhaften Schwellenwert von 8 Wiederholungen.</span><span class="sxs-lookup"><span data-stu-id="668f9-109">This command creates a health probe named Probe03, with HTTP protocol, a 30 second interval, timeout of 120 seconds, and an unhealthy threshold of 8 retries.</span></span>

## <span data-ttu-id="668f9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="668f9-110">PARAMETERS</span></span>

### <span data-ttu-id="668f9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="668f9-111">-DefaultProfile</span></span>
<span data-ttu-id="668f9-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="668f9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="668f9-113">-Hostname</span><span class="sxs-lookup"><span data-stu-id="668f9-113">-HostName</span></span>
<span data-ttu-id="668f9-114">Gibt den Hostnamen an, den dieses Cmdlet an die Sonde sendet.</span><span class="sxs-lookup"><span data-stu-id="668f9-114">Specifies the host name that this cmdlet sends the probe.</span></span>

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

### <span data-ttu-id="668f9-115">-Intervall</span><span class="sxs-lookup"><span data-stu-id="668f9-115">-Interval</span></span>
<span data-ttu-id="668f9-116">Gibt das Prüf punktintervall in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="668f9-116">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="668f9-117">Dies ist das Zeitintervall zwischen zwei aufeinanderfolgenden Prüfpunkten.</span><span class="sxs-lookup"><span data-stu-id="668f9-117">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="668f9-118">Dieser Wert liegt zwischen 1 Sekunde und 86400 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="668f9-118">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="668f9-119">-Vergleich</span><span class="sxs-lookup"><span data-stu-id="668f9-119">-Match</span></span>
<span data-ttu-id="668f9-120">Body, der in der Integritäts Antwort enthalten sein muss.</span><span class="sxs-lookup"><span data-stu-id="668f9-120">Body that must be contained in the health response.</span></span>
<span data-ttu-id="668f9-121">Der Standardwert ist leer</span><span class="sxs-lookup"><span data-stu-id="668f9-121">Default value is empty</span></span>

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

### <span data-ttu-id="668f9-122">-MinServers</span><span class="sxs-lookup"><span data-stu-id="668f9-122">-MinServers</span></span>
<span data-ttu-id="668f9-123">Minimale Anzahl von Servern, die immer als "fehlerfrei" gekennzeichnet sind.</span><span class="sxs-lookup"><span data-stu-id="668f9-123">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="668f9-124">Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="668f9-124">Default value is 0</span></span>

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

### <span data-ttu-id="668f9-125">-Name</span><span class="sxs-lookup"><span data-stu-id="668f9-125">-Name</span></span>
<span data-ttu-id="668f9-126">Gibt den Namen des Prüfpunkts an.</span><span class="sxs-lookup"><span data-stu-id="668f9-126">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="668f9-127">-Path</span><span class="sxs-lookup"><span data-stu-id="668f9-127">-Path</span></span>
<span data-ttu-id="668f9-128">Gibt den relativen Pfad des Prüfpunkts an.</span><span class="sxs-lookup"><span data-stu-id="668f9-128">Specifies the relative path of probe.</span></span>
<span data-ttu-id="668f9-129">Gültige Pfade beginnen mit dem Schrägstrich (/).</span><span class="sxs-lookup"><span data-stu-id="668f9-129">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="668f9-130">Die Sonde wird an \<Protocol\> :// \<host\> : gesendet \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="668f9-130">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="668f9-131">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="668f9-131">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="668f9-132">Gibt an, ob der Hostheader über die HTTP-Back-End-Einstellungen ausgewählt werden soll.</span><span class="sxs-lookup"><span data-stu-id="668f9-132">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="668f9-133">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="668f9-133">Default value is false</span></span>

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

### <span data-ttu-id="668f9-134">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="668f9-134">-Protocol</span></span>
<span data-ttu-id="668f9-135">Gibt das zum Senden der Sonde verwendete Protokoll an.</span><span class="sxs-lookup"><span data-stu-id="668f9-135">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="668f9-136">-Timeout</span><span class="sxs-lookup"><span data-stu-id="668f9-136">-Timeout</span></span>
<span data-ttu-id="668f9-137">Gibt das Prüfpunkt-Timeout in Sekunden an.</span><span class="sxs-lookup"><span data-stu-id="668f9-137">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="668f9-138">Dieses Cmdlet kennzeichnet die Prüfspitze als fehlerhaft, wenn bei diesem Timeoutzeitraum keine gültige Antwort empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="668f9-138">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="668f9-139">Gültige Werte liegen zwischen 1 Sekunde und 86400 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="668f9-139">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="668f9-140">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="668f9-140">-UnhealthyThreshold</span></span>
<span data-ttu-id="668f9-141">Gibt die Anzahl der Prüf Punkt Wiederholungen an.</span><span class="sxs-lookup"><span data-stu-id="668f9-141">Specifies the probe retry count.</span></span>
<span data-ttu-id="668f9-142">Der Back-End-Server wird markiert, nachdem der Fehlerzähler für aufeinanderfolgende Prüfpunkte den ungesunden Schwellenwert erreicht hat.</span><span class="sxs-lookup"><span data-stu-id="668f9-142">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="668f9-143">Gültige Werte liegen zwischen 1 Sekunde und 20 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="668f9-143">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="668f9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="668f9-144">CommonParameters</span></span>
<span data-ttu-id="668f9-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="668f9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="668f9-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="668f9-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="668f9-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="668f9-147">INPUTS</span></span>

### <span data-ttu-id="668f9-148">Keine</span><span class="sxs-lookup"><span data-stu-id="668f9-148">None</span></span>

## <span data-ttu-id="668f9-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="668f9-149">OUTPUTS</span></span>

### <span data-ttu-id="668f9-150">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="668f9-150">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="668f9-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="668f9-151">NOTES</span></span>

## <span data-ttu-id="668f9-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="668f9-152">RELATED LINKS</span></span>

[<span data-ttu-id="668f9-153">Erstellen eines benutzerdefinierten Prüfpunkts für das Anwendungs Gateway mit PowerShell für Azure Resource Manager</span><span class="sxs-lookup"><span data-stu-id="668f9-153">Create custom probe for Application Gateway using PowerShell for Azure Resource Manager</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#)

[<span data-ttu-id="668f9-154">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="668f9-154">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="668f9-155">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="668f9-155">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="668f9-156">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="668f9-156">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="668f9-157">Satz-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="668f9-157">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

