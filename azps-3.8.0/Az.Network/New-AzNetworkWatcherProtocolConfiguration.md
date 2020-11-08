---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherprotocolconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherProtocolConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherProtocolConfiguration.md
ms.openlocfilehash: 5358fa9898bca17f75c0111ef15b69e8cff4f75d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996537"
---
# <span data-ttu-id="85295-101">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="85295-101">New-AzNetworkWatcherProtocolConfiguration</span></span>

## <span data-ttu-id="85295-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="85295-102">SYNOPSIS</span></span>
<span data-ttu-id="85295-103">Erstellt ein neues Protokoll Konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="85295-103">Creates a new protocol configuration object.</span></span>

## <span data-ttu-id="85295-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="85295-104">SYNTAX</span></span>

```
New-AzNetworkWatcherProtocolConfiguration -Protocol <String> [-Method <String>] [-Header <IDictionary>]
 [-ValidStatusCode <Int32[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85295-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="85295-105">DESCRIPTION</span></span>
<span data-ttu-id="85295-106">Das New-AzNetworkWatcherProtocolConfiguration-Cmdlet erstellt ein neues Protokoll Konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="85295-106">The New-AzNetworkWatcherProtocolConfiguration cmdlet creates a new protocol configuration object.</span></span> <span data-ttu-id="85295-107">Dieses Objekt wird verwendet, um die Protokollkonfiguration während einer Verbindungs Überprüfungssitzung unter Verwendung der angegebenen Kriterien zu beschränken.</span><span class="sxs-lookup"><span data-stu-id="85295-107">This object is used to restrict the protocol configuration during a connectivity check session using the specified criteria.</span></span> 

## <span data-ttu-id="85295-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="85295-108">EXAMPLES</span></span>

### <span data-ttu-id="85295-109">Beispiel 1: Testen der Netzwerk Überwachungs Konnektivität von einem virtuellen Computer zu einer Website mit Protokollkonfiguration</span><span class="sxs-lookup"><span data-stu-id="85295-109">Example 1: Test Network Watcher Connectivity from a VM to a website with protocol configuration</span></span>
```
$config = New-AzNetworkWatcherProtocolConfiguration -Protocol Http -Method Get -Headers @{"accept"="application/json"} -ValidStatusCodes @(200,202,204)

Test-AzNetworkWatcherConnectivity -NetworkWatcherName NetworkWatcher -ResourceGroupName NetworkWatcherRG -SourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/providers/Microsoft.Compute/virtualMachines/MultiTierApp0" -DestinationAddress "bing.com" -DestinationPort 80 -ProtocolConfiguration $config


ConnectionStatus : Reachable
AvgLatencyInMs   : 4
MinLatencyInMs   : 2
MaxLatencyInMs   : 15
ProbesSent       : 15
ProbesFailed     : 0
Hops             : [
                     {
                       "Type": "Source",
                       "Id": "f8cff464-e13f-457f-a09e-4dcd53d38a85",
                       "Address": "10.1.1.4",
                       "ResourceId": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ContosoRG/provi                   iders/Microsoft.Network/networkInterfaces/appNic0/ipConfigurations/ipconfig1",
                       "NextHopIds": [
                         "1034b1bf-0b1b-4f0a-93b2-900477f45485"
                       ],
                       "Issues": []
                     },
                     {
                       "Type": "Internet",
                       "Id": "1034b1bf-0b1b-4f0a-93b2-900477f45485",
                       "Address": "13.107.21.200",
                       "ResourceId": "Internet",
                       "NextHopIds": [],
                       "Issues": []
                     }
                   ]
```

<span data-ttu-id="85295-110">In diesem Beispiel wird die Konnektivität von einem virtuellen Computer in Azure zu www.Bing.com getestet.</span><span class="sxs-lookup"><span data-stu-id="85295-110">In this example we test connectivity from a VM in Azure to www.bing.com.</span></span>

## <span data-ttu-id="85295-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="85295-111">PARAMETERS</span></span>

### <span data-ttu-id="85295-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85295-112">-DefaultProfile</span></span>
<span data-ttu-id="85295-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="85295-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85295-114">-Kopfzeile</span><span class="sxs-lookup"><span data-stu-id="85295-114">-Header</span></span>
<span data-ttu-id="85295-115">Liste der HTTP-Header</span><span class="sxs-lookup"><span data-stu-id="85295-115">list of HTTP headers</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85295-116">-Methode</span><span class="sxs-lookup"><span data-stu-id="85295-116">-Method</span></span>
<span data-ttu-id="85295-117">HTTP-Methode</span><span class="sxs-lookup"><span data-stu-id="85295-117">HTTP method</span></span>

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

### <span data-ttu-id="85295-118">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="85295-118">-Protocol</span></span>
<span data-ttu-id="85295-119">Protokolltyp</span><span class="sxs-lookup"><span data-stu-id="85295-119">Protocol type</span></span>

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

### <span data-ttu-id="85295-120">-ValidStatusCode</span><span class="sxs-lookup"><span data-stu-id="85295-120">-ValidStatusCode</span></span>
<span data-ttu-id="85295-121">gültige Statuscodes</span><span class="sxs-lookup"><span data-stu-id="85295-121">valid status codes</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85295-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85295-122">CommonParameters</span></span>
<span data-ttu-id="85295-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85295-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85295-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85295-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85295-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="85295-125">INPUTS</span></span>

### <span data-ttu-id="85295-126">Keine</span><span class="sxs-lookup"><span data-stu-id="85295-126">None</span></span>

## <span data-ttu-id="85295-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="85295-127">OUTPUTS</span></span>

### <span data-ttu-id="85295-128">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="85295-128">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherProtocolConfiguration</span></span>

## <span data-ttu-id="85295-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="85295-129">NOTES</span></span>
<span data-ttu-id="85295-130">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Watcher, Paket, Capture, Traffic, Filter</span><span class="sxs-lookup"><span data-stu-id="85295-130">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span>

## <span data-ttu-id="85295-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="85295-131">RELATED LINKS</span></span>

[<span data-ttu-id="85295-132">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="85295-132">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="85295-133">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="85295-133">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="85295-134">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="85295-134">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="85295-135">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="85295-135">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="85295-136">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="85295-136">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="85295-137">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="85295-137">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="85295-138">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="85295-138">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="85295-139">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="85295-139">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="85295-140">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="85295-140">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="85295-141">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="85295-141">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="85295-142">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="85295-142">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="85295-143">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="85295-143">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="85295-144">Neu – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="85295-144">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="85295-145">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="85295-145">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="85295-146">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="85295-146">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="85295-147">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="85295-147">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="85295-148">Anfang-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="85295-148">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="85295-149">Satz-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="85295-149">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="85295-150">Satz-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="85295-150">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="85295-151">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="85295-151">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="85295-152">Neu – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="85295-152">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="85295-153">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="85295-153">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="85295-154">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="85295-154">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="85295-155">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="85295-155">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="85295-156">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="85295-156">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="85295-157">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="85295-157">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="85295-158">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="85295-158">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
