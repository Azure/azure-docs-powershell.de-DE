---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherresourcetroubleshooting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
ms.openlocfilehash: 5c11eecb00aa97fc90aecc770a77285f77be988b
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100408473"
---
# <span data-ttu-id="40a88-101">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="40a88-101">Start-AzNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="40a88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40a88-102">SYNOPSIS</span></span>
<span data-ttu-id="40a88-103">Startet die Problembehandlung für eine Netzwerkressource in Azure.</span><span class="sxs-lookup"><span data-stu-id="40a88-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

## <span data-ttu-id="40a88-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="40a88-104">SYNTAX</span></span>

### <span data-ttu-id="40a88-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="40a88-105">SetByResource (Default)</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -StorageId <String> -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40a88-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="40a88-106">SetByName</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40a88-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="40a88-107">SetByLocation</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -Location <String> -TargetResourceId <String> -StorageId <String>
 -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40a88-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="40a88-108">DESCRIPTION</span></span>
<span data-ttu-id="40a88-109">Das Start-AzNetworkWatcherResourceTroubleshooting cmdlet startet die Problembehandlung für eine Netzwerkressource in Azure und gibt Informationen zu potenziellen Problemen und Problembehebungen zurück.</span><span class="sxs-lookup"><span data-stu-id="40a88-109">The Start-AzNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="40a88-110">Derzeit werden virtuelle Netzwerkgateways und Verbindungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="40a88-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="40a88-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="40a88-111">EXAMPLES</span></span>

### <span data-ttu-id="40a88-112">Beispiel 1: Starten der Problembehandlung auf einem virtuellen Netzwerkgateway</span><span class="sxs-lookup"><span data-stu-id="40a88-112">Example 1: Start Troubleshooting on a Virtual Network Gateway</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="40a88-113">Im obigen Beispiel wird die Problembehandlung auf einem virtuellen Netzwerkgateway gestartet.</span><span class="sxs-lookup"><span data-stu-id="40a88-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="40a88-114">Der Vorgang kann einige Minuten dauern.</span><span class="sxs-lookup"><span data-stu-id="40a88-114">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="40a88-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40a88-115">PARAMETERS</span></span>

### <span data-ttu-id="40a88-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40a88-116">-DefaultProfile</span></span>
<span data-ttu-id="40a88-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="40a88-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40a88-118">-Location</span><span class="sxs-lookup"><span data-stu-id="40a88-118">-Location</span></span>
<span data-ttu-id="40a88-119">Speicherort der Netzwerk-Watcher.</span><span class="sxs-lookup"><span data-stu-id="40a88-119">Location of the network watcher.</span></span>

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

### <span data-ttu-id="40a88-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="40a88-120">-NetworkWatcher</span></span>
<span data-ttu-id="40a88-121">Die Netzwerk-Watcher-Ressource.</span><span class="sxs-lookup"><span data-stu-id="40a88-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="40a88-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="40a88-122">-NetworkWatcherName</span></span>
<span data-ttu-id="40a88-123">Der Name der Netzwerk-Watcher.</span><span class="sxs-lookup"><span data-stu-id="40a88-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="40a88-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40a88-124">-ResourceGroupName</span></span>
<span data-ttu-id="40a88-125">Der Name der Ressourcengruppe "Netzwerk-Watcher".</span><span class="sxs-lookup"><span data-stu-id="40a88-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="40a88-126">-StorageId</span><span class="sxs-lookup"><span data-stu-id="40a88-126">-StorageId</span></span>
<span data-ttu-id="40a88-127">Die Speicher-ID.</span><span class="sxs-lookup"><span data-stu-id="40a88-127">The storage ID.</span></span>

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

### <span data-ttu-id="40a88-128">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="40a88-128">-StoragePath</span></span>
<span data-ttu-id="40a88-129">Der Speicherpfad.</span><span class="sxs-lookup"><span data-stu-id="40a88-129">The storage path.</span></span>

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

### <span data-ttu-id="40a88-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="40a88-130">-TargetResourceId</span></span>
<span data-ttu-id="40a88-131">Gibt die Ressourcen-ID der zu behandelnden Ressource an.</span><span class="sxs-lookup"><span data-stu-id="40a88-131">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="40a88-132">Beispielformat: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span><span class="sxs-lookup"><span data-stu-id="40a88-132">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="40a88-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40a88-133">CommonParameters</span></span>
<span data-ttu-id="40a88-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40a88-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40a88-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40a88-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40a88-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="40a88-136">INPUTS</span></span>

### <span data-ttu-id="40a88-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="40a88-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="40a88-138">System.String</span><span class="sxs-lookup"><span data-stu-id="40a88-138">System.String</span></span>

## <span data-ttu-id="40a88-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="40a88-139">OUTPUTS</span></span>

### <span data-ttu-id="40a88-140">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="40a88-140">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="40a88-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="40a88-141">NOTES</span></span>
<span data-ttu-id="40a88-142">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span><span class="sxs-lookup"><span data-stu-id="40a88-142">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="40a88-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="40a88-143">RELATED LINKS</span></span>

[<span data-ttu-id="40a88-144">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="40a88-144">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="40a88-145">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="40a88-145">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="40a88-146">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="40a88-146">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="40a88-147">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="40a88-147">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="40a88-148">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="40a88-148">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="40a88-149">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="40a88-149">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="40a88-150">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="40a88-150">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="40a88-151">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="40a88-151">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="40a88-152">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="40a88-152">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="40a88-153">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="40a88-153">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="40a88-154">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="40a88-154">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="40a88-155">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="40a88-155">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="40a88-156">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="40a88-156">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="40a88-157">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="40a88-157">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="40a88-158">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="40a88-158">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="40a88-159">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="40a88-159">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="40a88-160">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="40a88-160">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="40a88-161">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="40a88-161">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="40a88-162">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="40a88-162">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="40a88-163">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="40a88-163">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="40a88-164">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="40a88-164">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="40a88-165">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="40a88-165">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="40a88-166">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="40a88-166">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="40a88-167">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="40a88-167">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="40a88-168">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="40a88-168">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="40a88-169">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="40a88-169">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="40a88-170">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="40a88-170">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
