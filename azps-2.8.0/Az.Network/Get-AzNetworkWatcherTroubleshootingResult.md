---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchertroubleshootingresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
ms.openlocfilehash: 4f8fcbc0e5eee5aea92493b54acc631ffd144d3b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93821764"
---
# <span data-ttu-id="84b5d-101">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="84b5d-101">Get-AzNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="84b5d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="84b5d-102">SYNOPSIS</span></span>
<span data-ttu-id="84b5d-103">Ruft das Ergebnis der Problembehandlung aus dem zuvor ausgeführten oder zurzeit ausgeführten Problem behandlungsvorgang ab.</span><span class="sxs-lookup"><span data-stu-id="84b5d-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

## <span data-ttu-id="84b5d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="84b5d-104">SYNTAX</span></span>

### <span data-ttu-id="84b5d-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="84b5d-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84b5d-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="84b5d-106">SetByName</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84b5d-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="84b5d-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -Location <String> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84b5d-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="84b5d-108">DESCRIPTION</span></span>
<span data-ttu-id="84b5d-109">Das Get-AzNetworkWatcherTroubleshootingResult-Cmdlet ruft das Ergebnis der Problembehandlung aus dem zuvor ausgeführten oder aktuell ausgeführten Start-AzNetworkWatcherResourceTroubleshooting Vorgang ab.</span><span class="sxs-lookup"><span data-stu-id="84b5d-109">The Get-AzNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="84b5d-110">Wenn der Problem behandlungsvorgang gerade ausgeführt wird, kann dieser Vorgang einige Minuten dauern.</span><span class="sxs-lookup"><span data-stu-id="84b5d-110">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="84b5d-111">Derzeit werden virtuelle Netzwerkgateways und-Verbindungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="84b5d-111">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="84b5d-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="84b5d-112">EXAMPLES</span></span>

### <span data-ttu-id="84b5d-113">Beispiel 1: Starten der Problembehandlung auf einem virtuellen Netzwerk Gateway und Abrufen des Ergebnisses</span><span class="sxs-lookup"><span data-stu-id="84b5d-113">Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="84b5d-114">Im obigen Beispiel wird die Problembehandlung auf einem virtuellen Netzwerkgateway gestartet.</span><span class="sxs-lookup"><span data-stu-id="84b5d-114">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="84b5d-115">Es kann einige Minuten dauern, bis der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="84b5d-115">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="84b5d-116">Nachdem die Problembehandlung begonnen hat, wird ein Get-AzNetworkWatcherTroubleshootingResult Aufruf an die Ressource durchgeführt, um das Ergebnis dieses Anrufs abzurufen.</span><span class="sxs-lookup"><span data-stu-id="84b5d-116">After troubleshooting has started, a Get-AzNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="84b5d-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="84b5d-117">PARAMETERS</span></span>

### <span data-ttu-id="84b5d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84b5d-118">-DefaultProfile</span></span>
<span data-ttu-id="84b5d-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="84b5d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84b5d-120">-Standort</span><span class="sxs-lookup"><span data-stu-id="84b5d-120">-Location</span></span>
<span data-ttu-id="84b5d-121">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="84b5d-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="84b5d-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="84b5d-122">-NetworkWatcher</span></span>
<span data-ttu-id="84b5d-123">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="84b5d-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="84b5d-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="84b5d-124">-NetworkWatcherName</span></span>
<span data-ttu-id="84b5d-125">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="84b5d-125">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84b5d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84b5d-126">-ResourceGroupName</span></span>
<span data-ttu-id="84b5d-127">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="84b5d-127">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84b5d-128">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="84b5d-128">-TargetResourceId</span></span>
<span data-ttu-id="84b5d-129">Die Ziel Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="84b5d-129">The target resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84b5d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84b5d-130">CommonParameters</span></span>
<span data-ttu-id="84b5d-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84b5d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84b5d-132">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84b5d-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84b5d-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="84b5d-133">INPUTS</span></span>

### <span data-ttu-id="84b5d-134">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="84b5d-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="84b5d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="84b5d-135">System.String</span></span>

## <span data-ttu-id="84b5d-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="84b5d-136">OUTPUTS</span></span>

### <span data-ttu-id="84b5d-137">Microsoft. Azure. Commands. Network. Models. PSTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="84b5d-137">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="84b5d-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="84b5d-138">NOTES</span></span>
<span data-ttu-id="84b5d-139">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerkmonitor, Problembehandlung, VPN, Verbindung</span><span class="sxs-lookup"><span data-stu-id="84b5d-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="84b5d-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="84b5d-140">RELATED LINKS</span></span>

[<span data-ttu-id="84b5d-141">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="84b5d-141">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="84b5d-142">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="84b5d-142">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="84b5d-143">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="84b5d-143">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="84b5d-144">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="84b5d-144">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="84b5d-145">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="84b5d-145">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="84b5d-146">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="84b5d-146">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="84b5d-147">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="84b5d-147">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="84b5d-148">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="84b5d-148">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="84b5d-149">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="84b5d-149">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="84b5d-150">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="84b5d-150">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="84b5d-151">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="84b5d-151">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="84b5d-152">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="84b5d-152">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="84b5d-153">Neu – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="84b5d-153">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="84b5d-154">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="84b5d-154">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="84b5d-155">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="84b5d-155">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="84b5d-156">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="84b5d-156">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="84b5d-157">Anfang-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="84b5d-157">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="84b5d-158">Satz-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="84b5d-158">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="84b5d-159">Satz-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="84b5d-159">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="84b5d-160">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="84b5d-160">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="84b5d-161">Neu – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="84b5d-161">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="84b5d-162">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="84b5d-162">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="84b5d-163">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="84b5d-163">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="84b5d-164">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="84b5d-164">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="84b5d-165">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="84b5d-165">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="84b5d-166">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="84b5d-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="84b5d-167">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="84b5d-167">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
