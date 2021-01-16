---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: DE31891A-0EF7-44D7-B955-A3279D27CC21
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/new-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerProfile.md
ms.openlocfilehash: c5e1f69e8a11f09e4f7b838c5e489c8a240d40e6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98292984"
---
# <span data-ttu-id="1c277-101">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1c277-101">New-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="1c277-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c277-102">SYNOPSIS</span></span>
<span data-ttu-id="1c277-103">Erstellt ein Datenverkehrs-Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="1c277-103">Creates a Traffic Manager profile.</span></span>

## <span data-ttu-id="1c277-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1c277-104">SYNTAX</span></span>

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

## <span data-ttu-id="1c277-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1c277-105">DESCRIPTION</span></span>
<span data-ttu-id="1c277-106">Das **Cmdlet "New-AzTrafficManagerProfile"** erstellt ein Azure Traffic Manager-Profil.</span><span class="sxs-lookup"><span data-stu-id="1c277-106">The **New-AzTrafficManagerProfile** cmdlet creates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="1c277-107">Geben Sie den *Parameter "Name"* und die erforderlichen Einstellungen an.</span><span class="sxs-lookup"><span data-stu-id="1c277-107">Specify the *Name* parameter and required settings.</span></span>
<span data-ttu-id="1c277-108">Dieses Cmdlet gibt ein lokales Objekt zurück, das das neue Profil darstellt.</span><span class="sxs-lookup"><span data-stu-id="1c277-108">This cmdlet returns a local object that represents the new profile.</span></span>

<span data-ttu-id="1c277-109">Mit diesem Cmdlet werden keine Endpunkte für Verkehrs-Manager konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="1c277-109">This cmdlet does not configure Traffic Manager endpoints.</span></span>
<span data-ttu-id="1c277-110">Sie können das lokale Profilobjekt mithilfe des cmdlets Add-AzTrafficManagerEndpointConfig aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="1c277-110">You can update the local profile object by using the Add-AzTrafficManagerEndpointConfig cmdlet.</span></span>
<span data-ttu-id="1c277-111">Laden Sie dann Änderungen in Traffic Manager mithilfe des Set-AzTrafficManagerProfile Hochlade-Cmdlets hoch.</span><span class="sxs-lookup"><span data-stu-id="1c277-111">Then upload changes to Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="1c277-112">Alternativ können Sie Endpunkte mithilfe des cmdlets New-AzTrafficManagerEndpoint hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1c277-112">Alternatively, you can add endpoints by using the New-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="1c277-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1c277-113">EXAMPLES</span></span>

### <span data-ttu-id="1c277-114">Beispiel 1: Erstellen eines Profils</span><span class="sxs-lookup"><span data-stu-id="1c277-114">Example 1: Create a profile</span></span>
```
PS C:\>New-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" -ProfileStatus Enabled -TrafficRoutingMethod Performance -RelativeDnsName "contosoapp" -TTL 30 -MonitorProtocol HTTP -MonitorPort 80 -MonitorPath "/default.aspx"
```

<span data-ttu-id="1c277-115">Mit diesem Befehl wird ein Azure Traffic -Manager-Profil namens "ContosoProfile" in der Ressourcengruppe "ResourceGroup11" erstellt.</span><span class="sxs-lookup"><span data-stu-id="1c277-115">This command creates an Azure Traffic Manager profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="1c277-116">Der DNS-FQDN ist contosoapp.trafficmanager.net.</span><span class="sxs-lookup"><span data-stu-id="1c277-116">The DNS FQDN is contosoapp.trafficmanager.net.</span></span>

## <span data-ttu-id="1c277-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c277-117">PARAMETERS</span></span>

### <span data-ttu-id="1c277-118">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="1c277-118">-CustomHeader</span></span>
<span data-ttu-id="1c277-119">Liste von benutzerdefinierten Headernamen- und Wertpaaren für Probeanforderungen.</span><span class="sxs-lookup"><span data-stu-id="1c277-119">List of custom header name and value pairs for probe requests.</span></span>

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

### <span data-ttu-id="1c277-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c277-120">-DefaultProfile</span></span>
<span data-ttu-id="1c277-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1c277-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c277-122">-ExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="1c277-122">-ExpectedStatusCodeRange</span></span>
<span data-ttu-id="1c277-123">Liste der erwarteten HTTP-Statuscodebereiche für Probeanforderungen.</span><span class="sxs-lookup"><span data-stu-id="1c277-123">List of expected HTTP status code ranges for probe requests.</span></span>

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

### <span data-ttu-id="1c277-124">-MaxReturn</span><span class="sxs-lookup"><span data-stu-id="1c277-124">-MaxReturn</span></span>
<span data-ttu-id="1c277-125">Die maximale Anzahl von Antworten, die für Profile mit einer mehrwertigen Routingmethode zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1c277-125">The maximum number of answers returned for profiles with a MultiValue routing method.</span></span>

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

### <span data-ttu-id="1c277-126">-MonitorIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="1c277-126">-MonitorIntervalInSeconds</span></span>
<span data-ttu-id="1c277-127">Das Intervall (in Sekunden), in dem der Verkehrsmanager die Integrität der einzelnen Endpunkte in diesem Profil überprüft.</span><span class="sxs-lookup"><span data-stu-id="1c277-127">The interval (in seconds) at which Traffic Manager will check the health of each endpoint in this profile.</span></span> <span data-ttu-id="1c277-128">Der Standardwert ist 30.</span><span class="sxs-lookup"><span data-stu-id="1c277-128">The default is 30.</span></span>

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

### <span data-ttu-id="1c277-129">-MonitorPath</span><span class="sxs-lookup"><span data-stu-id="1c277-129">-MonitorPath</span></span>
<span data-ttu-id="1c277-130">Gibt den Pfad an, der zum Überwachen des Endpunktzustands verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1c277-130">Specifies the path that is used to monitor endpoint health.</span></span>
<span data-ttu-id="1c277-131">Geben Sie einen Wert relativ zum Domänennamen des Endpunkts an.</span><span class="sxs-lookup"><span data-stu-id="1c277-131">Specify a value relative to the endpoint domain name.</span></span>
<span data-ttu-id="1c277-132">Dieser Wert muss mit einem Schrägstrich (/) beginnen.</span><span class="sxs-lookup"><span data-stu-id="1c277-132">This value must begin with a slash (/).</span></span>

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

### <span data-ttu-id="1c277-133">-MonitorPort</span><span class="sxs-lookup"><span data-stu-id="1c277-133">-MonitorPort</span></span>
<span data-ttu-id="1c277-134">Gibt den TCP-Port an, der zum Überwachen des Endpunktzustands verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1c277-134">Specifies the TCP port that is used to monitor endpoint health.</span></span>
<span data-ttu-id="1c277-135">Gültige Werte sind ganze Zahlen zwischen 1 und 65535.</span><span class="sxs-lookup"><span data-stu-id="1c277-135">Valid values are integers from 1 through 65535.</span></span>

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

### <span data-ttu-id="1c277-136">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="1c277-136">-MonitorProtocol</span></span>
<span data-ttu-id="1c277-137">Gibt das Protokoll an, das zum Überwachen des Endpunktzustands verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1c277-137">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="1c277-138">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="1c277-138">Valid values are:</span></span>

- <span data-ttu-id="1c277-139">HTTP</span><span class="sxs-lookup"><span data-stu-id="1c277-139">HTTP</span></span>
- <span data-ttu-id="1c277-140">HTTPS</span><span class="sxs-lookup"><span data-stu-id="1c277-140">HTTPS</span></span>

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

### <span data-ttu-id="1c277-141">-MonitorTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="1c277-141">-MonitorTimeoutInSeconds</span></span>
<span data-ttu-id="1c277-142">Die Uhrzeit (in Sekunden), zu der der Verkehrs-Manager Endpunkten in diesem Profil erlaubt, auf die Integritätsprüfung zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="1c277-142">The time (in seconds) that Traffic Manager allows endpoints in this profile to respond to the health check.</span></span> <span data-ttu-id="1c277-143">Der Standardwert ist 10.</span><span class="sxs-lookup"><span data-stu-id="1c277-143">The default is 10.</span></span>

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

### <span data-ttu-id="1c277-144">-MonitorTonumberOfFailures</span><span class="sxs-lookup"><span data-stu-id="1c277-144">-MonitorToleratedNumberOfFailures</span></span>
<span data-ttu-id="1c277-145">Die Anzahl der aufeinander folgenden fehlgeschlagenen Integritätsprüfungen, die von Traffic Manager vor dem Deklarieren eines Endpunkts in diesem Profil nach der nächsten fehlgeschlagenen Integritätsprüfung degradiert wurden.</span><span class="sxs-lookup"><span data-stu-id="1c277-145">The number of consecutive failed health checks that Traffic Manager tolerates before declaring an endpoint in this profile Degraded after the next consecutive failed health check.</span></span> <span data-ttu-id="1c277-146">Der Standardwert ist "3".</span><span class="sxs-lookup"><span data-stu-id="1c277-146">The default is 3.</span></span>

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

### <span data-ttu-id="1c277-147">-Name</span><span class="sxs-lookup"><span data-stu-id="1c277-147">-Name</span></span>
<span data-ttu-id="1c277-148">Gibt einen Namen für das Datenverkehrs-Manager-Profil an, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="1c277-148">Specifies a name for the Traffic Manager profile that this cmdlet creates.</span></span>

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

### <span data-ttu-id="1c277-149">-ProfileStatus</span><span class="sxs-lookup"><span data-stu-id="1c277-149">-ProfileStatus</span></span>
<span data-ttu-id="1c277-150">Gibt den Status des Profils an.</span><span class="sxs-lookup"><span data-stu-id="1c277-150">Specifies the status of the profile.</span></span>
<span data-ttu-id="1c277-151">Gültige Werte sind: Aktiviert und deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="1c277-151">Valid values are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="1c277-152">-RelativeDnsName</span><span class="sxs-lookup"><span data-stu-id="1c277-152">-RelativeDnsName</span></span>
<span data-ttu-id="1c277-153">Gibt den relativen DNS-Namen an, der in diesem Datenverkehrs-Manager-Profil angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1c277-153">Specifies the relative DNS name that this Traffic Manager profile provides.</span></span>
<span data-ttu-id="1c277-154">Traffic Manager kombiniert diesen Wert und den DNS-Domänennamen, den Azure Traffic Manager verwendet, um den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des Profils zu bilden.</span><span class="sxs-lookup"><span data-stu-id="1c277-154">Traffic Manager combines this value and the DNS domain name that Azure Traffic Manager uses to form the fully qualified domain name (FQDN) of the profile.</span></span>

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

### <span data-ttu-id="1c277-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c277-155">-ResourceGroupName</span></span>
<span data-ttu-id="1c277-156">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="1c277-156">Specifies the name of a resource group.</span></span>
<span data-ttu-id="1c277-157">Dieses Cmdlet erstellt ein Traffic -Manager-Profil in der Gruppe, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="1c277-157">This cmdlet creates a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1c277-158">-Tag</span><span class="sxs-lookup"><span data-stu-id="1c277-158">-Tag</span></span>
<span data-ttu-id="1c277-159">Schlüssel-Wert-Paare in Form einer Hashtabelle, die als Tags auf dem Server festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1c277-159">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="1c277-160">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="1c277-160">For example:</span></span>

<span data-ttu-id="1c277-161">@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="1c277-161">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1c277-162">-TrafficRoutingMethod</span><span class="sxs-lookup"><span data-stu-id="1c277-162">-TrafficRoutingMethod</span></span>
<span data-ttu-id="1c277-163">Gibt die Datenverkehrsroutingmethode an.</span><span class="sxs-lookup"><span data-stu-id="1c277-163">Specifies the traffic routing method.</span></span>
<span data-ttu-id="1c277-164">Diese Methode bestimmt, welcher Endpunkt Traffic Manager als Reaktion auf eingehende DNS-Abfragen zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="1c277-164">This method determines which endpoint Traffic Manager returns in response to incoming DNS queries.</span></span>
<span data-ttu-id="1c277-165">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="1c277-165">Valid values are:</span></span>

- <span data-ttu-id="1c277-166">Leistung</span><span class="sxs-lookup"><span data-stu-id="1c277-166">Performance</span></span>
- <span data-ttu-id="1c277-167">Gewichtet</span><span class="sxs-lookup"><span data-stu-id="1c277-167">Weighted</span></span>
- <span data-ttu-id="1c277-168">Priorität</span><span class="sxs-lookup"><span data-stu-id="1c277-168">Priority</span></span>
- <span data-ttu-id="1c277-169">Geografisch</span><span class="sxs-lookup"><span data-stu-id="1c277-169">Geographic</span></span>

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

### <span data-ttu-id="1c277-170">-Ttl</span><span class="sxs-lookup"><span data-stu-id="1c277-170">-Ttl</span></span>
<span data-ttu-id="1c277-171">Gibt den Wert für "DNS Time to Live (TTL)" an.</span><span class="sxs-lookup"><span data-stu-id="1c277-171">Specifies the DNS Time to Live (TTL) value.</span></span>

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

### <span data-ttu-id="1c277-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c277-172">CommonParameters</span></span>
<span data-ttu-id="1c277-173">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c277-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c277-174">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c277-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c277-175">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1c277-175">INPUTS</span></span>

### <span data-ttu-id="1c277-176">Keine</span><span class="sxs-lookup"><span data-stu-id="1c277-176">None</span></span>

## <span data-ttu-id="1c277-177">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1c277-177">OUTPUTS</span></span>

### <span data-ttu-id="1c277-178">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1c277-178">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="1c277-179">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1c277-179">NOTES</span></span>

## <span data-ttu-id="1c277-180">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1c277-180">RELATED LINKS</span></span>

[<span data-ttu-id="1c277-181">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="1c277-181">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="1c277-182">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1c277-182">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="1c277-183">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1c277-183">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="1c277-184">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1c277-184">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="1c277-185">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1c277-185">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="1c277-186">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="1c277-186">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


