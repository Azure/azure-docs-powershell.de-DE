---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkwatchertroubleshootingresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherTroubleshootingResult.md
ms.openlocfilehash: 49c7dc8359d0745f54aa94dc5cd1e7ce9a0e2307
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919752"
---
# <span data-ttu-id="f8f1b-101">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="f8f1b-101">Get-AzNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="f8f1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8f1b-102">SYNOPSIS</span></span>
<span data-ttu-id="f8f1b-103">Ruft das Problembehandlungsergebnis aus dem zuvor ausgeführten oder aktuell ausgeführten Problembehandlungsvorgang ab.</span><span class="sxs-lookup"><span data-stu-id="f8f1b-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

## <span data-ttu-id="f8f1b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f8f1b-104">SYNTAX</span></span>

### <span data-ttu-id="f8f1b-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="f8f1b-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8f1b-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="f8f1b-106">SetByName</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8f1b-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="f8f1b-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherTroubleshootingResult -Location <String> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8f1b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f8f1b-108">DESCRIPTION</span></span>
<span data-ttu-id="f8f1b-109">Das Get-AzNetworkWatcherTroubleshootingResult-Cmdlet ruft das Problembehandlungsergebnis aus dem zuvor ausgeführten oder aktuell ausgeführten Start-AzNetworkWatcherResourceTroubleshooting ab.</span><span class="sxs-lookup"><span data-stu-id="f8f1b-109">The Get-AzNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="f8f1b-110">Wenn der Problembehandlungsvorgang zurzeit ausgeführt wird, kann dieser Vorgang einige Minuten dauern.</span><span class="sxs-lookup"><span data-stu-id="f8f1b-110">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="f8f1b-111">Derzeit werden Gateways und Verbindungen für virtuelle Netzwerke unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f8f1b-111">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="f8f1b-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f8f1b-112">EXAMPLES</span></span>

### <span data-ttu-id="f8f1b-113">Beispiel 1: Starten der Problembehandlung auf einem Virtuellen Netzwerkgateway und Abrufen des Ergebnisses</span><span class="sxs-lookup"><span data-stu-id="f8f1b-113">Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="f8f1b-114">Im vorstehenden Beispiel wird die Problembehandlung auf einem Gateway für virtuelle Netzwerke gestartet.</span><span class="sxs-lookup"><span data-stu-id="f8f1b-114">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="f8f1b-115">Der Vorgang kann einige Minuten dauern.</span><span class="sxs-lookup"><span data-stu-id="f8f1b-115">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="f8f1b-116">Nachdem die Problembehandlung gestartet wurde, Get-AzNetworkWatcherTroubleshootingResult die Ressource aufgerufen, um das Ergebnis dieses Aufrufs abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f8f1b-116">After troubleshooting has started, a Get-AzNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="f8f1b-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f8f1b-117">PARAMETERS</span></span>

### <span data-ttu-id="f8f1b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8f1b-118">-DefaultProfile</span></span>
<span data-ttu-id="f8f1b-119">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f8f1b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8f1b-120">-Location</span><span class="sxs-lookup"><span data-stu-id="f8f1b-120">-Location</span></span>
<span data-ttu-id="f8f1b-121">Speicherort des Netzwerkwächters.</span><span class="sxs-lookup"><span data-stu-id="f8f1b-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="f8f1b-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f8f1b-122">-NetworkWatcher</span></span>
<span data-ttu-id="f8f1b-123">Die Netzwerkwächterressource.</span><span class="sxs-lookup"><span data-stu-id="f8f1b-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="f8f1b-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="f8f1b-124">-NetworkWatcherName</span></span>
<span data-ttu-id="f8f1b-125">Der Name des Netzwerkwächters.</span><span class="sxs-lookup"><span data-stu-id="f8f1b-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="f8f1b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8f1b-126">-ResourceGroupName</span></span>
<span data-ttu-id="f8f1b-127">Der Name der Ressourcengruppe "Netzwerkwächter".</span><span class="sxs-lookup"><span data-stu-id="f8f1b-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="f8f1b-128">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="f8f1b-128">-TargetResourceId</span></span>
<span data-ttu-id="f8f1b-129">Die Zielressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="f8f1b-129">The target resource ID.</span></span>

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

### <span data-ttu-id="f8f1b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8f1b-130">CommonParameters</span></span>
<span data-ttu-id="f8f1b-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8f1b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8f1b-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8f1b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8f1b-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f8f1b-133">INPUTS</span></span>

### <span data-ttu-id="f8f1b-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f8f1b-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="f8f1b-135">System.String</span><span class="sxs-lookup"><span data-stu-id="f8f1b-135">System.String</span></span>

## <span data-ttu-id="f8f1b-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f8f1b-136">OUTPUTS</span></span>

### <span data-ttu-id="f8f1b-137">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="f8f1b-137">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="f8f1b-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f8f1b-138">NOTES</span></span>
<span data-ttu-id="f8f1b-139">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span><span class="sxs-lookup"><span data-stu-id="f8f1b-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="f8f1b-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f8f1b-140">RELATED LINKS</span></span>

[<span data-ttu-id="f8f1b-141">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f8f1b-141">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="f8f1b-142">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f8f1b-142">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="f8f1b-143">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f8f1b-143">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="f8f1b-144">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f8f1b-144">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="f8f1b-145">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f8f1b-145">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="f8f1b-146">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f8f1b-146">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="f8f1b-147">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f8f1b-147">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="f8f1b-148">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f8f1b-148">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f8f1b-149">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f8f1b-149">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="f8f1b-150">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f8f1b-150">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f8f1b-151">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f8f1b-151">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f8f1b-152">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f8f1b-152">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f8f1b-153">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8f1b-153">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="f8f1b-154">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f8f1b-154">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="f8f1b-155">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="f8f1b-155">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="f8f1b-156">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f8f1b-156">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f8f1b-157">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f8f1b-157">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f8f1b-158">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f8f1b-158">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f8f1b-159">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="f8f1b-159">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="f8f1b-160">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f8f1b-160">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f8f1b-161">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f8f1b-161">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="f8f1b-162">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="f8f1b-162">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="f8f1b-163">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="f8f1b-163">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="f8f1b-164">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="f8f1b-164">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="f8f1b-165">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="f8f1b-165">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="f8f1b-166">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="f8f1b-166">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="f8f1b-167">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="f8f1b-167">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
