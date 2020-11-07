---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 71227c2e351e12381a857dcf9cd66767f00265cd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822304"
---
# <span data-ttu-id="3d53f-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="3d53f-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="3d53f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3d53f-102">SYNOPSIS</span></span>
<span data-ttu-id="3d53f-103">Ruft den relativen Latenz Faktor für Internetdienstanbieter von einem angegebenen Speicherort zu Azure-Regionen ab.</span><span class="sxs-lookup"><span data-stu-id="3d53f-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="3d53f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d53f-104">SYNTAX</span></span>

### <span data-ttu-id="3d53f-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="3d53f-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <String[]>] [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d53f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="3d53f-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d53f-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3d53f-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String> [-Provider <String[]>] [-Location <String[]>]
 -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3d53f-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="3d53f-108">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherLocation <String> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d53f-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3d53f-109">DESCRIPTION</span></span>
<span data-ttu-id="3d53f-110">Der Get-AzNetworkWatcherReachabilityReport ruft den relativen Latenz Faktor für Internetdienstanbieter von einem angegebenen Speicherort zu Azure-Regionen ab.</span><span class="sxs-lookup"><span data-stu-id="3d53f-110">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="3d53f-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3d53f-111">EXAMPLES</span></span>

### <span data-ttu-id="3d53f-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3d53f-112">Example 1</span></span>
```
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

<span data-ttu-id="3d53f-113">Ruft relative Latenzen für das Azure-Rechenzentrum in West-US von 2017-10-10 bis 2017-10-12 innerhalb des United-Bundesstaates ab.</span><span class="sxs-lookup"><span data-stu-id="3d53f-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="3d53f-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d53f-114">PARAMETERS</span></span>

### <span data-ttu-id="3d53f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d53f-115">-AsJob</span></span>
<span data-ttu-id="3d53f-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3d53f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3d53f-117">-Ort</span><span class="sxs-lookup"><span data-stu-id="3d53f-117">-City</span></span>
<span data-ttu-id="3d53f-118">Der Name des Orts.</span><span class="sxs-lookup"><span data-stu-id="3d53f-118">The name of the city.</span></span>

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

### <span data-ttu-id="3d53f-119">-Land</span><span class="sxs-lookup"><span data-stu-id="3d53f-119">-Country</span></span>
<span data-ttu-id="3d53f-120">Der Name des Landes.</span><span class="sxs-lookup"><span data-stu-id="3d53f-120">The name of the country.</span></span>

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

### <span data-ttu-id="3d53f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d53f-121">-DefaultProfile</span></span>
<span data-ttu-id="3d53f-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3d53f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d53f-123">-EndTime</span><span class="sxs-lookup"><span data-stu-id="3d53f-123">-EndTime</span></span>
<span data-ttu-id="3d53f-124">Die Endzeit für den Azure-Erreichbarkeits Bericht.</span><span class="sxs-lookup"><span data-stu-id="3d53f-124">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="3d53f-125">-Standort</span><span class="sxs-lookup"><span data-stu-id="3d53f-125">-Location</span></span>
<span data-ttu-id="3d53f-126">Optionale Azure-Bereiche zum Bereich der Abfrage.</span><span class="sxs-lookup"><span data-stu-id="3d53f-126">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="3d53f-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3d53f-127">-NetworkWatcher</span></span>
<span data-ttu-id="3d53f-128">Die Netzwerk Überwachungsressource</span><span class="sxs-lookup"><span data-stu-id="3d53f-128">The network watcher resource</span></span>

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

### <span data-ttu-id="3d53f-129">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="3d53f-129">-NetworkWatcherLocation</span></span>
<span data-ttu-id="3d53f-130">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="3d53f-130">Location of the network watcher.</span></span>

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

### <span data-ttu-id="3d53f-131">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="3d53f-131">-NetworkWatcherName</span></span>
<span data-ttu-id="3d53f-132">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="3d53f-132">The name of network watcher.</span></span>

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

### <span data-ttu-id="3d53f-133">-Anbieter</span><span class="sxs-lookup"><span data-stu-id="3d53f-133">-Provider</span></span>
<span data-ttu-id="3d53f-134">Liste der Internet Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="3d53f-134">List of Internet service providers.</span></span>

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

### <span data-ttu-id="3d53f-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d53f-135">-ResourceGroupName</span></span>
<span data-ttu-id="3d53f-136">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="3d53f-136">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="3d53f-137">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3d53f-137">-ResourceId</span></span>
<span data-ttu-id="3d53f-138">Die ID der Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="3d53f-138">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="3d53f-139">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="3d53f-139">-StartTime</span></span>
<span data-ttu-id="3d53f-140">Die Startzeit für den Azure-Erreichbarkeits Bericht.</span><span class="sxs-lookup"><span data-stu-id="3d53f-140">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="3d53f-141">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="3d53f-141">-State</span></span>
<span data-ttu-id="3d53f-142">Der Name des Zustands.</span><span class="sxs-lookup"><span data-stu-id="3d53f-142">The name of the state.</span></span>

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

### <span data-ttu-id="3d53f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d53f-143">CommonParameters</span></span>
<span data-ttu-id="3d53f-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d53f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d53f-145">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d53f-145">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d53f-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3d53f-146">INPUTS</span></span>

### <span data-ttu-id="3d53f-147">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3d53f-147">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="3d53f-148">System. String</span><span class="sxs-lookup"><span data-stu-id="3d53f-148">System.String</span></span>

## <span data-ttu-id="3d53f-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3d53f-149">OUTPUTS</span></span>

### <span data-ttu-id="3d53f-150">Microsoft. Azure. Commands. Network. Models. PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="3d53f-150">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="3d53f-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="3d53f-151">NOTES</span></span>
<span data-ttu-id="3d53f-152">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerkmonitor, Erreichbarkeit, Bericht</span><span class="sxs-lookup"><span data-stu-id="3d53f-152">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="3d53f-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3d53f-153">RELATED LINKS</span></span>

[<span data-ttu-id="3d53f-154">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3d53f-154">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="3d53f-155">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3d53f-155">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="3d53f-156">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3d53f-156">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="3d53f-157">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="3d53f-157">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="3d53f-158">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="3d53f-158">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="3d53f-159">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="3d53f-159">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="3d53f-160">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="3d53f-160">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="3d53f-161">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3d53f-161">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3d53f-162">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="3d53f-162">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="3d53f-163">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3d53f-163">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3d53f-164">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3d53f-164">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3d53f-165">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3d53f-165">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3d53f-166">Neu – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d53f-166">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="3d53f-167">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="3d53f-167">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="3d53f-168">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="3d53f-168">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="3d53f-169">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3d53f-169">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3d53f-170">Anfang-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3d53f-170">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3d53f-171">Satz-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3d53f-171">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3d53f-172">Satz-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="3d53f-172">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="3d53f-173">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3d53f-173">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3d53f-174">Neu – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3d53f-174">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3d53f-175">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="3d53f-175">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="3d53f-176">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="3d53f-176">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="3d53f-177">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="3d53f-177">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="3d53f-178">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="3d53f-178">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="3d53f-179">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="3d53f-179">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="3d53f-180">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3d53f-180">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)