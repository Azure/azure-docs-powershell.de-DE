---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 3fe26c99dd92afb65105008524908a10dec02e0e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178550"
---
# <span data-ttu-id="03948-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="03948-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="03948-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="03948-102">SYNOPSIS</span></span>
<span data-ttu-id="03948-103">Ruft den relativen Latenz Faktor für Internetdienstanbieter von einem angegebenen Speicherort zu Azure-Regionen ab.</span><span class="sxs-lookup"><span data-stu-id="03948-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="03948-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="03948-104">SYNTAX</span></span>

### <span data-ttu-id="03948-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="03948-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <String[]>] [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03948-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="03948-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03948-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="03948-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String> [-Provider <String[]>] [-Location <String[]>]
 -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03948-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="03948-108">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherLocation <String> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03948-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="03948-109">DESCRIPTION</span></span>
<span data-ttu-id="03948-110">Der Get-AzNetworkWatcherReachabilityReport ruft den relativen Latenz Faktor für Internetdienstanbieter von einem angegebenen Speicherort zu Azure-Regionen ab.</span><span class="sxs-lookup"><span data-stu-id="03948-110">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="03948-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="03948-111">EXAMPLES</span></span>

### <span data-ttu-id="03948-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="03948-112">Example 1</span></span>
```powershell
$nw = Get-AzNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher $nw -Location "West US" -Country "United States" -StartTime "2017-10-10" -EndTime "2017-10-12"

"aggregationLevel" : "Country",
"providerLocation" : {
    "country" : "United States"
},
"reachabilityReport" : [
    {
        "provider" : "Frontier Communications of America, Inc. - ASN 5650",
        "azureLocation": "West US",
        "latencies": [
            {
                "timeStamp": "2017-10-10T00:00:00Z",
                "score": 94
            },
            {
                "timeStamp": "2017-10-11T00:00:00Z",
                "score": 94
            },
            {
                "timeStamp": "2017-10-12T00:00:00Z",
                "score": 94    
            }
        ]  
    }
]
```

<span data-ttu-id="03948-113">Ruft relative Latenzen für das Azure-Rechenzentrum in West-US von 2017-10-10 bis 2017-10-12 innerhalb des United-Bundesstaates ab.</span><span class="sxs-lookup"><span data-stu-id="03948-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

### <span data-ttu-id="03948-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="03948-114">Example 2</span></span>

<span data-ttu-id="03948-115">Ruft den relativen Latenz Faktor für Internetdienstanbieter von einem angegebenen Speicherort zu Azure-Regionen ab.</span><span class="sxs-lookup"><span data-stu-id="03948-115">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span> <span data-ttu-id="03948-116">automatisch</span><span class="sxs-lookup"><span data-stu-id="03948-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNetworkWatcherReachabilityReport -Country 'United States' -EndTime '2017-10-12' -Location 'West US' -NetworkWatcherName nw1 -ResourceGroupName myresourcegroup -StartTime '2017-10-10' -State 'washington'
```

## <span data-ttu-id="03948-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="03948-117">PARAMETERS</span></span>

### <span data-ttu-id="03948-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03948-118">-AsJob</span></span>
<span data-ttu-id="03948-119">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="03948-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="03948-120">-Ort</span><span class="sxs-lookup"><span data-stu-id="03948-120">-City</span></span>
<span data-ttu-id="03948-121">Der Name des Orts.</span><span class="sxs-lookup"><span data-stu-id="03948-121">The name of the city.</span></span>

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

### <span data-ttu-id="03948-122">-Land</span><span class="sxs-lookup"><span data-stu-id="03948-122">-Country</span></span>
<span data-ttu-id="03948-123">Der Name des Landes.</span><span class="sxs-lookup"><span data-stu-id="03948-123">The name of the country.</span></span>

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

### <span data-ttu-id="03948-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03948-124">-DefaultProfile</span></span>
<span data-ttu-id="03948-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="03948-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03948-126">-EndTime</span><span class="sxs-lookup"><span data-stu-id="03948-126">-EndTime</span></span>
<span data-ttu-id="03948-127">Die Endzeit für den Azure-Erreichbarkeits Bericht.</span><span class="sxs-lookup"><span data-stu-id="03948-127">The end time for the Azure reachability report.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03948-128">-Standort</span><span class="sxs-lookup"><span data-stu-id="03948-128">-Location</span></span>
<span data-ttu-id="03948-129">Optionale Azure-Bereiche zum Bereich der Abfrage.</span><span class="sxs-lookup"><span data-stu-id="03948-129">Optional Azure regions to scope the query to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03948-130">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="03948-130">-NetworkWatcher</span></span>
<span data-ttu-id="03948-131">Die Netzwerk Überwachungsressource</span><span class="sxs-lookup"><span data-stu-id="03948-131">The network watcher resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03948-132">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="03948-132">-NetworkWatcherLocation</span></span>
<span data-ttu-id="03948-133">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="03948-133">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03948-134">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="03948-134">-NetworkWatcherName</span></span>
<span data-ttu-id="03948-135">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="03948-135">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: ResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03948-136">-Anbieter</span><span class="sxs-lookup"><span data-stu-id="03948-136">-Provider</span></span>
<span data-ttu-id="03948-137">Liste der Internet Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="03948-137">List of Internet service providers.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03948-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03948-138">-ResourceGroupName</span></span>
<span data-ttu-id="03948-139">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="03948-139">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03948-140">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="03948-140">-ResourceId</span></span>
<span data-ttu-id="03948-141">Die ID der Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="03948-141">The Id of network watcher resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03948-142">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="03948-142">-StartTime</span></span>
<span data-ttu-id="03948-143">Die Startzeit für den Azure-Erreichbarkeits Bericht.</span><span class="sxs-lookup"><span data-stu-id="03948-143">The start time for the Azure reachability report.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03948-144">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="03948-144">-State</span></span>
<span data-ttu-id="03948-145">Der Name des Zustands.</span><span class="sxs-lookup"><span data-stu-id="03948-145">The name of the state.</span></span>

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

### <span data-ttu-id="03948-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03948-146">CommonParameters</span></span>
<span data-ttu-id="03948-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03948-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03948-148">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="03948-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03948-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="03948-149">INPUTS</span></span>

### <span data-ttu-id="03948-150">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="03948-150">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="03948-151">System. String</span><span class="sxs-lookup"><span data-stu-id="03948-151">System.String</span></span>

## <span data-ttu-id="03948-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="03948-152">OUTPUTS</span></span>

### <span data-ttu-id="03948-153">Microsoft. Azure. Commands. Network. Models. PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="03948-153">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="03948-154">Notizen</span><span class="sxs-lookup"><span data-stu-id="03948-154">NOTES</span></span>
<span data-ttu-id="03948-155">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerkmonitor, Erreichbarkeit, Bericht</span><span class="sxs-lookup"><span data-stu-id="03948-155">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="03948-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="03948-156">RELATED LINKS</span></span>

[<span data-ttu-id="03948-157">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="03948-157">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="03948-158">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="03948-158">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="03948-159">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="03948-159">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="03948-160">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="03948-160">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="03948-161">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="03948-161">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="03948-162">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="03948-162">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="03948-163">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="03948-163">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="03948-164">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="03948-164">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="03948-165">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="03948-165">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="03948-166">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="03948-166">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="03948-167">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="03948-167">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="03948-168">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="03948-168">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="03948-169">Neu – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="03948-169">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="03948-170">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="03948-170">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="03948-171">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="03948-171">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="03948-172">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="03948-172">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="03948-173">Anfang-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="03948-173">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="03948-174">Satz-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="03948-174">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="03948-175">Satz-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="03948-175">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="03948-176">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="03948-176">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="03948-177">Neu – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="03948-177">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="03948-178">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="03948-178">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="03948-179">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="03948-179">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="03948-180">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="03948-180">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="03948-181">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="03948-181">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="03948-182">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="03948-182">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="03948-183">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="03948-183">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
