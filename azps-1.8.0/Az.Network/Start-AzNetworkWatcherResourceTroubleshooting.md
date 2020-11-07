---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-aznetworkwatcherresourcetroubleshooting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzNetworkWatcherResourceTroubleshooting.md
ms.openlocfilehash: 5399c97f076f1402b20b91798d2db215d00af8b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660148"
---
# <span data-ttu-id="ce9ef-101">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="ce9ef-101">Start-AzNetworkWatcherResourceTroubleshooting</span></span>

## <span data-ttu-id="ce9ef-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ce9ef-102">SYNOPSIS</span></span>
<span data-ttu-id="ce9ef-103">Startet die Problembehandlung für eine Netzwerkressource in Azure.</span><span class="sxs-lookup"><span data-stu-id="ce9ef-103">Starts troubleshooting on a Networking resource in Azure.</span></span>

## <span data-ttu-id="ce9ef-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce9ef-104">SYNTAX</span></span>

### <span data-ttu-id="ce9ef-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="ce9ef-105">SetByResource (Default)</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -StorageId <String> -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce9ef-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="ce9ef-106">SetByName</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -StorageId <String> -StoragePath <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce9ef-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="ce9ef-107">SetByLocation</span></span>
```
Start-AzNetworkWatcherResourceTroubleshooting -Location <String> -TargetResourceId <String> -StorageId <String>
 -StoragePath <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce9ef-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ce9ef-108">DESCRIPTION</span></span>
<span data-ttu-id="ce9ef-109">Das Start-AzNetworkWatcherResourceTroubleshooting-Cmdlet startet die Problembehandlung für eine Netzwerkressource in Azure und gibt Informationen zu potenziellen Problemen und Abschwächungen zurück.</span><span class="sxs-lookup"><span data-stu-id="ce9ef-109">The Start-AzNetworkWatcherResourceTroubleshooting cmdlet starts troubleshooting for a Networking resource in Azure and returns information about potential issues and mitigations.</span></span> <span data-ttu-id="ce9ef-110">Derzeit werden virtuelle Netzwerkgateways und-Verbindungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ce9ef-110">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="ce9ef-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ce9ef-111">EXAMPLES</span></span>

### <span data-ttu-id="ce9ef-112">Beispiel 1: Starten der Problembehandlung auf einem virtuellen Netzwerk Gateway</span><span class="sxs-lookup"><span data-stu-id="ce9ef-112">Example 1: Start Troubleshooting on a Virtual Network Gateway</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath
```

<span data-ttu-id="ce9ef-113">Im obigen Beispiel wird die Problembehandlung auf einem virtuellen Netzwerkgateway gestartet.</span><span class="sxs-lookup"><span data-stu-id="ce9ef-113">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="ce9ef-114">Es kann einige Minuten dauern, bis der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="ce9ef-114">The operation may take a few minutes to complete.</span></span>

## <span data-ttu-id="ce9ef-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce9ef-115">PARAMETERS</span></span>

### <span data-ttu-id="ce9ef-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce9ef-116">-DefaultProfile</span></span>
<span data-ttu-id="ce9ef-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ce9ef-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce9ef-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="ce9ef-118">-Location</span></span>
<span data-ttu-id="ce9ef-119">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="ce9ef-119">Location of the network watcher.</span></span>

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

### <span data-ttu-id="ce9ef-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ce9ef-120">-NetworkWatcher</span></span>
<span data-ttu-id="ce9ef-121">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="ce9ef-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="ce9ef-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="ce9ef-122">-NetworkWatcherName</span></span>
<span data-ttu-id="ce9ef-123">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="ce9ef-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="ce9ef-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce9ef-124">-ResourceGroupName</span></span>
<span data-ttu-id="ce9ef-125">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="ce9ef-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="ce9ef-126">-Speicher-Nr</span><span class="sxs-lookup"><span data-stu-id="ce9ef-126">-StorageId</span></span>
<span data-ttu-id="ce9ef-127">Die Speicher-ID.</span><span class="sxs-lookup"><span data-stu-id="ce9ef-127">The storage ID.</span></span>

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

### <span data-ttu-id="ce9ef-128">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="ce9ef-128">-StoragePath</span></span>
<span data-ttu-id="ce9ef-129">Der Speicherpfad.</span><span class="sxs-lookup"><span data-stu-id="ce9ef-129">The storage path.</span></span>

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

### <span data-ttu-id="ce9ef-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="ce9ef-130">-TargetResourceId</span></span>
<span data-ttu-id="ce9ef-131">Gibt die Ressourcen-ID der zu behandelnden Ressource an.</span><span class="sxs-lookup"><span data-stu-id="ce9ef-131">Specifies the resource id of the resource to troubleshoot.</span></span> <span data-ttu-id="ce9ef-132">Beispielformat: "/Subscriptions/$ {Subscription-Nr}/resourceGroups/$ {resourceGroupName}/Providers/Microsoft.Network/Connections/$ {ConnectionName}"</span><span class="sxs-lookup"><span data-stu-id="ce9ef-132">Example format: "/subscriptions/${subscriptionId}/resourceGroups/${resourceGroupName}/providers/Microsoft.Network/connections/${connectionName}"</span></span>

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

### <span data-ttu-id="ce9ef-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce9ef-133">CommonParameters</span></span>
<span data-ttu-id="ce9ef-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce9ef-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce9ef-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce9ef-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce9ef-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ce9ef-136">INPUTS</span></span>

### <span data-ttu-id="ce9ef-137">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ce9ef-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="ce9ef-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ce9ef-138">System.String</span></span>

## <span data-ttu-id="ce9ef-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ce9ef-139">OUTPUTS</span></span>

### <span data-ttu-id="ce9ef-140">Microsoft. Azure. Commands. Network. Models. PSTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="ce9ef-140">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="ce9ef-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="ce9ef-141">NOTES</span></span>
<span data-ttu-id="ce9ef-142">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerkmonitor, Problembehandlung, VPN, Verbindung</span><span class="sxs-lookup"><span data-stu-id="ce9ef-142">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="ce9ef-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ce9ef-143">RELATED LINKS</span></span>

[<span data-ttu-id="ce9ef-144">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ce9ef-144">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="ce9ef-145">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ce9ef-145">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="ce9ef-146">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ce9ef-146">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="ce9ef-147">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="ce9ef-147">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="ce9ef-148">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="ce9ef-148">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="ce9ef-149">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="ce9ef-149">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="ce9ef-150">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="ce9ef-150">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="ce9ef-151">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ce9ef-151">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ce9ef-152">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ce9ef-152">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="ce9ef-153">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ce9ef-153">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ce9ef-154">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ce9ef-154">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ce9ef-155">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ce9ef-155">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ce9ef-156">Neu – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="ce9ef-156">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="ce9ef-157">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="ce9ef-157">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="ce9ef-158">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="ce9ef-158">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="ce9ef-159">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ce9ef-159">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ce9ef-160">Anfang-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ce9ef-160">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ce9ef-161">Satz-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ce9ef-161">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ce9ef-162">Satz-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="ce9ef-162">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="ce9ef-163">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ce9ef-163">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ce9ef-164">Neu – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ce9ef-164">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ce9ef-165">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="ce9ef-165">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="ce9ef-166">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="ce9ef-166">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="ce9ef-167">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="ce9ef-167">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="ce9ef-168">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="ce9ef-168">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="ce9ef-169">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="ce9ef-169">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="ce9ef-170">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ce9ef-170">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)