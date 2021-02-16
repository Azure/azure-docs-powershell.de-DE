---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: f29ab593ffac847ec6b089efdc39bc594ad1d785
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412366"
---
# <span data-ttu-id="79e96-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="79e96-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="79e96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79e96-102">SYNOPSIS</span></span>
<span data-ttu-id="79e96-103">Ruft den relativen Latenzpunkt für Internetdienstanbieter von einem angegebenen Speicherort in die Regionen von Azure ab.</span><span class="sxs-lookup"><span data-stu-id="79e96-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="79e96-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="79e96-104">SYNTAX</span></span>

### <span data-ttu-id="79e96-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="79e96-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <String[]>] [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79e96-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="79e96-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79e96-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="79e96-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String> [-Provider <String[]>] [-Location <String[]>]
 -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79e96-108">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="79e96-108">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherLocation <String> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79e96-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="79e96-109">DESCRIPTION</span></span>
<span data-ttu-id="79e96-110">Die Get-AzNetworkWatcherReachabilityReport ruft den relativen Latenzpunkt für Internetdienstanbieter von einem angegebenen Speicherort in die Regionen von Azure ab.</span><span class="sxs-lookup"><span data-stu-id="79e96-110">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="79e96-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="79e96-111">EXAMPLES</span></span>

### <span data-ttu-id="79e96-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="79e96-112">Example 1</span></span>
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

<span data-ttu-id="79e96-113">Ruft relative Latenzen für das Azure Data Center im Westen der USA vom 10.10.2017 bis zum 12.10.2017 innerhalb der USA ab.</span><span class="sxs-lookup"><span data-stu-id="79e96-113">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

### <span data-ttu-id="79e96-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="79e96-114">Example 2</span></span>

<span data-ttu-id="79e96-115">Ruft den relativen Latenzpunkt für Internetdienstanbieter von einem angegebenen Speicherort in die Regionen von Azure ab.</span><span class="sxs-lookup"><span data-stu-id="79e96-115">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span> <span data-ttu-id="79e96-116">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="79e96-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNetworkWatcherReachabilityReport -Country 'United States' -EndTime '2017-10-12' -Location 'West US' -NetworkWatcherName nw1 -ResourceGroupName myresourcegroup -StartTime '2017-10-10' -State 'washington'
```

## <span data-ttu-id="79e96-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79e96-117">PARAMETERS</span></span>

### <span data-ttu-id="79e96-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79e96-118">-AsJob</span></span>
<span data-ttu-id="79e96-119">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="79e96-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="79e96-120">-Ort</span><span class="sxs-lookup"><span data-stu-id="79e96-120">-City</span></span>
<span data-ttu-id="79e96-121">Der Name der Stadt.</span><span class="sxs-lookup"><span data-stu-id="79e96-121">The name of the city.</span></span>

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

### <span data-ttu-id="79e96-122">-Country</span><span class="sxs-lookup"><span data-stu-id="79e96-122">-Country</span></span>
<span data-ttu-id="79e96-123">Der Name des Landes.</span><span class="sxs-lookup"><span data-stu-id="79e96-123">The name of the country.</span></span>

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

### <span data-ttu-id="79e96-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79e96-124">-DefaultProfile</span></span>
<span data-ttu-id="79e96-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="79e96-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79e96-126">-EndTime</span><span class="sxs-lookup"><span data-stu-id="79e96-126">-EndTime</span></span>
<span data-ttu-id="79e96-127">Die Endzeit für den Azure-Erreichbarkeitsbericht.</span><span class="sxs-lookup"><span data-stu-id="79e96-127">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="79e96-128">-Location</span><span class="sxs-lookup"><span data-stu-id="79e96-128">-Location</span></span>
<span data-ttu-id="79e96-129">Optionale Azure-Regionen, auf die die Abfrage begrenzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="79e96-129">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="79e96-130">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="79e96-130">-NetworkWatcher</span></span>
<span data-ttu-id="79e96-131">Die Netzwerk-Watcher-Ressource</span><span class="sxs-lookup"><span data-stu-id="79e96-131">The network watcher resource</span></span>

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

### <span data-ttu-id="79e96-132">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="79e96-132">-NetworkWatcherLocation</span></span>
<span data-ttu-id="79e96-133">Speicherort der Netzwerk-Watcher.</span><span class="sxs-lookup"><span data-stu-id="79e96-133">Location of the network watcher.</span></span>

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

### <span data-ttu-id="79e96-134">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="79e96-134">-NetworkWatcherName</span></span>
<span data-ttu-id="79e96-135">Der Name der Netzwerk-Watcher.</span><span class="sxs-lookup"><span data-stu-id="79e96-135">The name of network watcher.</span></span>

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

### <span data-ttu-id="79e96-136">-Provider</span><span class="sxs-lookup"><span data-stu-id="79e96-136">-Provider</span></span>
<span data-ttu-id="79e96-137">Liste der Internetdienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="79e96-137">List of Internet service providers.</span></span>

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

### <span data-ttu-id="79e96-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79e96-138">-ResourceGroupName</span></span>
<span data-ttu-id="79e96-139">Der Name der Ressourcengruppe "Netzwerk-Watcher".</span><span class="sxs-lookup"><span data-stu-id="79e96-139">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="79e96-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79e96-140">-ResourceId</span></span>
<span data-ttu-id="79e96-141">Die ID der Netzwerk-Watcher-Ressource.</span><span class="sxs-lookup"><span data-stu-id="79e96-141">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="79e96-142">-StartTime</span><span class="sxs-lookup"><span data-stu-id="79e96-142">-StartTime</span></span>
<span data-ttu-id="79e96-143">Die Startzeit für den Azure-Erreichbarkeitsbericht.</span><span class="sxs-lookup"><span data-stu-id="79e96-143">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="79e96-144">-State</span><span class="sxs-lookup"><span data-stu-id="79e96-144">-State</span></span>
<span data-ttu-id="79e96-145">Der Name des Zustands.</span><span class="sxs-lookup"><span data-stu-id="79e96-145">The name of the state.</span></span>

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

### <span data-ttu-id="79e96-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79e96-146">CommonParameters</span></span>
<span data-ttu-id="79e96-147">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79e96-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79e96-148">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="79e96-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79e96-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="79e96-149">INPUTS</span></span>

### <span data-ttu-id="79e96-150">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="79e96-150">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="79e96-151">System.String</span><span class="sxs-lookup"><span data-stu-id="79e96-151">System.String</span></span>

## <span data-ttu-id="79e96-152">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="79e96-152">OUTPUTS</span></span>

### <span data-ttu-id="79e96-153">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="79e96-153">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="79e96-154">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="79e96-154">NOTES</span></span>
<span data-ttu-id="79e96-155">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span><span class="sxs-lookup"><span data-stu-id="79e96-155">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="79e96-156">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="79e96-156">RELATED LINKS</span></span>

[<span data-ttu-id="79e96-157">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="79e96-157">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="79e96-158">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="79e96-158">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="79e96-159">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="79e96-159">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="79e96-160">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="79e96-160">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="79e96-161">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="79e96-161">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="79e96-162">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="79e96-162">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="79e96-163">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="79e96-163">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="79e96-164">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="79e96-164">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="79e96-165">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="79e96-165">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="79e96-166">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="79e96-166">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="79e96-167">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="79e96-167">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="79e96-168">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="79e96-168">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="79e96-169">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="79e96-169">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="79e96-170">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="79e96-170">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="79e96-171">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="79e96-171">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="79e96-172">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="79e96-172">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="79e96-173">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="79e96-173">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="79e96-174">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="79e96-174">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="79e96-175">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="79e96-175">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="79e96-176">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="79e96-176">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="79e96-177">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="79e96-177">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="79e96-178">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="79e96-178">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="79e96-179">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="79e96-179">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="79e96-180">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="79e96-180">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="79e96-181">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="79e96-181">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="79e96-182">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="79e96-182">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="79e96-183">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="79e96-183">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
