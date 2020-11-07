---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: DE31891A-0EF7-44D7-B955-A3279D27CC21
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/new-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerProfile.md
ms.openlocfilehash: aed780d75280f38ba8fa99052c3af0cd8bbe9612
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93827044"
---
# <span data-ttu-id="3f6e4-101">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3f6e4-101">New-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="3f6e4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3f6e4-102">SYNOPSIS</span></span>
<span data-ttu-id="3f6e4-103">Erstellt ein Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-103">Creates a Traffic Manager profile.</span></span>

## <span data-ttu-id="3f6e4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f6e4-104">SYNTAX</span></span>

```
New-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-ProfileStatus <String>]
 -RelativeDnsName <String> -Ttl <UInt32> -TrafficRoutingMethod <String> -MonitorProtocol <String>
 -MonitorPort <UInt32> [-MonitorPath <String>] [-MonitorIntervalInSeconds <Int32>]
 [-MonitorTimeoutInSeconds <Int32>] [-MonitorToleratedNumberOfFailures <Int32>] [-MaxReturn <Int64>]
 [-Tag <Hashtable>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-ExpectedStatusCodeRange <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerExpectedStatusCodeRange]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f6e4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3f6e4-105">DESCRIPTION</span></span>
<span data-ttu-id="3f6e4-106">Das Cmdlet **New-AzTrafficManagerProfile** erstellt ein Azure Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-106">The **New-AzTrafficManagerProfile** cmdlet creates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="3f6e4-107">Geben Sie den Parameter *Name* und die erforderlichen Einstellungen an.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-107">Specify the *Name* parameter and required settings.</span></span>
<span data-ttu-id="3f6e4-108">Dieses Cmdlet gibt ein lokales Objekt zurück, das das neue Profil darstellt.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-108">This cmdlet returns a local object that represents the new profile.</span></span>

<span data-ttu-id="3f6e4-109">Dieses Cmdlet konfiguriert keine Datenverkehrs-Manager-Endpunkte.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-109">This cmdlet does not configure Traffic Manager endpoints.</span></span>
<span data-ttu-id="3f6e4-110">Sie können das lokale Profilobjekt mithilfe des Add-AzTrafficManagerEndpointConfig-Cmdlets aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-110">You can update the local profile object by using the Add-AzTrafficManagerEndpointConfig cmdlet.</span></span>
<span data-ttu-id="3f6e4-111">Laden Sie dann Änderungen an Traffic Manager mithilfe des Set-AzTrafficManagerProfile-Cmdlets hoch.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-111">Then upload changes to Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="3f6e4-112">Sie können Endpunkte auch mithilfe des New-AzTrafficManagerEndpoint-Cmdlets hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-112">Alternatively, you can add endpoints by using the New-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="3f6e4-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3f6e4-113">EXAMPLES</span></span>

### <span data-ttu-id="3f6e4-114">Beispiel 1: Erstellen eines Profils</span><span class="sxs-lookup"><span data-stu-id="3f6e4-114">Example 1: Create a profile</span></span>
```
PS C:\>New-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" -ProfileStatus Enabled -TrafficRoutingMethod Performance -RelativeDnsName "contosoapp" -TTL 30 -MonitorProtocol HTTP -MonitorPort 80 -MonitorPath "/default.aspx"
```

<span data-ttu-id="3f6e4-115">Dieser Befehl erstellt ein Azure Traffic Manager-Profil mit dem Namen ContosoProfile in der Ressourcengruppen-ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-115">This command creates an Azure Traffic Manager profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="3f6e4-116">Der DNS-FQDN lautet contosoapp.Trafficmanager.net.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-116">The DNS FQDN is contosoapp.trafficmanager.net.</span></span>

## <span data-ttu-id="3f6e4-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f6e4-117">PARAMETERS</span></span>

### <span data-ttu-id="3f6e4-118">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="3f6e4-118">-CustomHeader</span></span>
<span data-ttu-id="3f6e4-119">Liste der benutzerdefinierten Headername-und Wert-Paare für Prüf Punkt Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3f6e4-119">List of custom header name and value pairs for probe requests.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f6e4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f6e4-120">-DefaultProfile</span></span>
<span data-ttu-id="3f6e4-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f6e4-122">-ExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="3f6e4-122">-ExpectedStatusCodeRange</span></span>
<span data-ttu-id="3f6e4-123">Liste der erwarteten HTTP-Statuscode Bereiche für Prüf Punkt Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3f6e4-123">List of expected HTTP status code ranges for probe requests.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerExpectedStatusCodeRange]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f6e4-124">-MaxReturn</span><span class="sxs-lookup"><span data-stu-id="3f6e4-124">-MaxReturn</span></span>
<span data-ttu-id="3f6e4-125">Die maximale Anzahl von Antworten, die für Profile mit einer mehrwertigen Routingmethode zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-125">The maximum number of answers returned for profiles with a MultiValue routing method.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f6e4-126">-MonitorIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="3f6e4-126">-MonitorIntervalInSeconds</span></span>
<span data-ttu-id="3f6e4-127">Das Intervall (in Sekunden), in dem der Datenverkehrs-Manager die Integrität der einzelnen Endpunkt in diesem Profil überprüft.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-127">The interval (in seconds) at which Traffic Manager will check the health of each endpoint in this profile.</span></span> <span data-ttu-id="3f6e4-128">Der Standardwert ist 30.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-128">The default is 30.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: IntervalInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f6e4-129">-MonitorPath</span><span class="sxs-lookup"><span data-stu-id="3f6e4-129">-MonitorPath</span></span>
<span data-ttu-id="3f6e4-130">Gibt den Pfad an, der zum Überwachen des Endpunkt Zustands verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-130">Specifies the path that is used to monitor endpoint health.</span></span>
<span data-ttu-id="3f6e4-131">Geben Sie einen Wert relativ zum Endpunkt Domänennamen an.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-131">Specify a value relative to the endpoint domain name.</span></span>
<span data-ttu-id="3f6e4-132">Dieser Wert muss mit einem Schrägstrich (/) beginnen.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-132">This value must begin with a slash (/).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PathForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f6e4-133">-MonitorPort</span><span class="sxs-lookup"><span data-stu-id="3f6e4-133">-MonitorPort</span></span>
<span data-ttu-id="3f6e4-134">Gibt den TCP-Port an, der zum Überwachen des Endpunkt Zustands verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-134">Specifies the TCP port that is used to monitor endpoint health.</span></span>
<span data-ttu-id="3f6e4-135">Gültige Werte sind ganze Zahlen von 1 bis 65535.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-135">Valid values are integers from 1 through 65535.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases: PortForMonitor

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f6e4-136">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="3f6e4-136">-MonitorProtocol</span></span>
<span data-ttu-id="3f6e4-137">Gibt das Protokoll an, das zum Überwachen der Endpunkt Integrität verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-137">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="3f6e4-138">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="3f6e4-138">Valid values are:</span></span>

- <span data-ttu-id="3f6e4-139">HTTP</span><span class="sxs-lookup"><span data-stu-id="3f6e4-139">HTTP</span></span>
- <span data-ttu-id="3f6e4-140">HTTPS</span><span class="sxs-lookup"><span data-stu-id="3f6e4-140">HTTPS</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProtocolForMonitor
Accepted values: HTTP, HTTPS, TCP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f6e4-141">-MonitorTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="3f6e4-141">-MonitorTimeoutInSeconds</span></span>
<span data-ttu-id="3f6e4-142">Die Zeit (in Sekunden), die der Datenverkehrs-Manager Endpunkten in diesem Profil ermöglicht, auf die Integritätsprüfung zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-142">The time (in seconds) that Traffic Manager allows endpoints in this profile to respond to the health check.</span></span> <span data-ttu-id="3f6e4-143">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-143">The default is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: TimeoutInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f6e4-144">-MonitorToleratedNumberOfFailures</span><span class="sxs-lookup"><span data-stu-id="3f6e4-144">-MonitorToleratedNumberOfFailures</span></span>
<span data-ttu-id="3f6e4-145">Die Anzahl der aufeinander folgenden fehlgeschlagenen Integritätsprüfungen, die vom Datenverkehrs Manager toleriert werden, bevor ein Endpunkt in diesem Profil nach der nächsten fehlgeschlagenen Integritätsprüfung in Folgefehler Haft deklariert wird.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-145">The number of consecutive failed health checks that Traffic Manager tolerates before declaring an endpoint in this profile Degraded after the next consecutive failed health check.</span></span> <span data-ttu-id="3f6e4-146">Der Standardwert ist 3.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-146">The default is 3.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ToleratedNumberOfFailuresForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f6e4-147">-Name</span><span class="sxs-lookup"><span data-stu-id="3f6e4-147">-Name</span></span>
<span data-ttu-id="3f6e4-148">Gibt einen Namen für das von diesem Cmdlet erstellte Datenverkehrs-Manager-Profil an.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-148">Specifies a name for the Traffic Manager profile that this cmdlet creates.</span></span>

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

### <span data-ttu-id="3f6e4-149">-ProfileStatus</span><span class="sxs-lookup"><span data-stu-id="3f6e4-149">-ProfileStatus</span></span>
<span data-ttu-id="3f6e4-150">Gibt den Status des Profils an.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-150">Specifies the status of the profile.</span></span>
<span data-ttu-id="3f6e4-151">Gültige Werte sind: Enabled und Disabled.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-151">Valid values are: Enabled and Disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f6e4-152">-RelativeDnsName</span><span class="sxs-lookup"><span data-stu-id="3f6e4-152">-RelativeDnsName</span></span>
<span data-ttu-id="3f6e4-153">Gibt den relativen DNS-Namen an, der in diesem Datenverkehrs-Manager-Profil bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-153">Specifies the relative DNS name that this Traffic Manager profile provides.</span></span>
<span data-ttu-id="3f6e4-154">Traffic Manager kombiniert diesen Wert und den DNS-Domänennamen, den Azure Traffic Manager verwendet, um den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des Profils zu bilden.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-154">Traffic Manager combines this value and the DNS domain name that Azure Traffic Manager uses to form the fully qualified domain name (FQDN) of the profile.</span></span>

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

### <span data-ttu-id="3f6e4-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f6e4-155">-ResourceGroupName</span></span>
<span data-ttu-id="3f6e4-156">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-156">Specifies the name of a resource group.</span></span>
<span data-ttu-id="3f6e4-157">Mit diesem Cmdlet wird ein Datenverkehrs-Manager-Profil in der Gruppe erstellt, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-157">This cmdlet creates a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3f6e4-158">-Tag</span><span class="sxs-lookup"><span data-stu-id="3f6e4-158">-Tag</span></span>
<span data-ttu-id="3f6e4-159">Schlüssel-Wert-Paare in Form einer Hashtabelle, die als Tags auf dem Server definiert ist.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-159">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="3f6e4-160">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="3f6e4-160">For example:</span></span>

<span data-ttu-id="3f6e4-161">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="3f6e4-161">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f6e4-162">-TrafficRoutingMethod</span><span class="sxs-lookup"><span data-stu-id="3f6e4-162">-TrafficRoutingMethod</span></span>
<span data-ttu-id="3f6e4-163">Gibt die Datenverkehrs Routingmethode an.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-163">Specifies the traffic routing method.</span></span>
<span data-ttu-id="3f6e4-164">Diese Methode bestimmt, welcher Endpunkt Datenverkehrs-Manager als Antwort auf eingehende DNS-Abfragen zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-164">This method determines which endpoint Traffic Manager returns in response to incoming DNS queries.</span></span>
<span data-ttu-id="3f6e4-165">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="3f6e4-165">Valid values are:</span></span>

- <span data-ttu-id="3f6e4-166">Leistung</span><span class="sxs-lookup"><span data-stu-id="3f6e4-166">Performance</span></span>
- <span data-ttu-id="3f6e4-167">Gewichteten</span><span class="sxs-lookup"><span data-stu-id="3f6e4-167">Weighted</span></span>
- <span data-ttu-id="3f6e4-168">Priorität</span><span class="sxs-lookup"><span data-stu-id="3f6e4-168">Priority</span></span>
- <span data-ttu-id="3f6e4-169">Geografische</span><span class="sxs-lookup"><span data-stu-id="3f6e4-169">Geographic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Performance, Weighted, Priority, Geographic, Subnet, MultiValue

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f6e4-170">-TTL</span><span class="sxs-lookup"><span data-stu-id="3f6e4-170">-Ttl</span></span>
<span data-ttu-id="3f6e4-171">Gibt den Wert für DNS Time to Live (TTL) an.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-171">Specifies the DNS Time to Live (TTL) value.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f6e4-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f6e4-172">CommonParameters</span></span>
<span data-ttu-id="3f6e4-173">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f6e4-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f6e4-174">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f6e4-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f6e4-175">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3f6e4-175">INPUTS</span></span>

### <span data-ttu-id="3f6e4-176">Keine</span><span class="sxs-lookup"><span data-stu-id="3f6e4-176">None</span></span>

## <span data-ttu-id="3f6e4-177">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3f6e4-177">OUTPUTS</span></span>

### <span data-ttu-id="3f6e4-178">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3f6e4-178">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="3f6e4-179">Notizen</span><span class="sxs-lookup"><span data-stu-id="3f6e4-179">NOTES</span></span>

## <span data-ttu-id="3f6e4-180">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3f6e4-180">RELATED LINKS</span></span>

[<span data-ttu-id="3f6e4-181">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="3f6e4-181">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="3f6e4-182">Deaktivieren-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3f6e4-182">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="3f6e4-183">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3f6e4-183">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="3f6e4-184">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3f6e4-184">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="3f6e4-185">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3f6e4-185">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="3f6e4-186">Satz-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3f6e4-186">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


