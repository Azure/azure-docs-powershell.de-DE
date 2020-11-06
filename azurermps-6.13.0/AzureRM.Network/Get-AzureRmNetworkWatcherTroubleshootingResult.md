---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchertroubleshootingresult
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherTroubleshootingResult.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherTroubleshootingResult.md
ms.openlocfilehash: 527d0fd33629ed7e1fcecdd23ba7cf8c93822f16
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503545"
---
# <span data-ttu-id="d006a-101">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="d006a-101">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>

## <span data-ttu-id="d006a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d006a-102">SYNOPSIS</span></span>
<span data-ttu-id="d006a-103">Ruft das Ergebnis der Problembehandlung aus dem zuvor ausgeführten oder zurzeit ausgeführten Problem behandlungsvorgang ab.</span><span class="sxs-lookup"><span data-stu-id="d006a-103">Gets the troubleshooting result from the previously run or currently running troubleshooting operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d006a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d006a-104">SYNTAX</span></span>

### <span data-ttu-id="d006a-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="d006a-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d006a-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="d006a-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d006a-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="d006a-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherTroubleshootingResult -Location <String> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d006a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d006a-108">DESCRIPTION</span></span>
<span data-ttu-id="d006a-109">Das Get-AzureRmNetworkWatcherTroubleshootingResult-Cmdlet ruft das Ergebnis der Problembehandlung aus dem zuvor ausgeführten oder aktuell ausgeführten Start-AzureRmNetworkWatcherResourceTroubleshooting Vorgang ab.</span><span class="sxs-lookup"><span data-stu-id="d006a-109">The Get-AzureRmNetworkWatcherTroubleshootingResult cmdlet gets the troubleshooting result from the previously run or currently running Start-AzureRmNetworkWatcherResourceTroubleshooting operation.</span></span> <span data-ttu-id="d006a-110">Wenn der Problem behandlungsvorgang gerade ausgeführt wird, kann dieser Vorgang einige Minuten dauern.</span><span class="sxs-lookup"><span data-stu-id="d006a-110">If the troubleshooting operation is currently in progress, then this operation may take a few minutes to complete.</span></span> <span data-ttu-id="d006a-111">Derzeit werden virtuelle Netzwerkgateways und-Verbindungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d006a-111">Currently Virtual Network Gateways and Connections are supported.</span></span>

## <span data-ttu-id="d006a-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d006a-112">EXAMPLES</span></span>

### <span data-ttu-id="d006a-113">Beispiel 1: Starten der Problembehandlung auf einem virtuellen Netzwerk Gateway und Abrufen des Ergebnisses</span><span class="sxs-lookup"><span data-stu-id="d006a-113">Example 1: Start Troubleshooting on a Virtual Network Gateway and Retrieve Result</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$target = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworkGateways/{vnetGatewayName}'
$storageId = '/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{storageAccountName}'
$storagePath = 'https://{storageAccountName}.blob.core.windows.net/troubleshoot'

Start-AzureRmNetworkWatcherResourceTroubleshooting -NetworkWatcher $networkWatcher -TargetResourceId $target -StorageId $storageId -StoragePath $storagePath

Get-AzureRmNetworkWatcherTroubleshootingResult -NetworkWatcher $NW -TargetResourceId $target
```

<span data-ttu-id="d006a-114">Im obigen Beispiel wird die Problembehandlung auf einem virtuellen Netzwerkgateway gestartet.</span><span class="sxs-lookup"><span data-stu-id="d006a-114">The above sample starts troubleshooting on a virtual network gateway.</span></span> <span data-ttu-id="d006a-115">Es kann einige Minuten dauern, bis der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="d006a-115">The operation may take a few minutes to complete.</span></span>
<span data-ttu-id="d006a-116">Nachdem die Problembehandlung begonnen hat, wird ein Get-AzureRmNetworkWatcherTroubleshootingResult Aufruf an die Ressource durchgeführt, um das Ergebnis dieses Anrufs abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d006a-116">After troubleshooting has started, a Get-AzureRmNetworkWatcherTroubleshootingResult call is made to the resource to retrieve the result of this call.</span></span> 

## <span data-ttu-id="d006a-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="d006a-117">PARAMETERS</span></span>

### <span data-ttu-id="d006a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d006a-118">-DefaultProfile</span></span>
<span data-ttu-id="d006a-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d006a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d006a-120">-Standort</span><span class="sxs-lookup"><span data-stu-id="d006a-120">-Location</span></span>
<span data-ttu-id="d006a-121">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="d006a-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="d006a-122">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d006a-122">-NetworkWatcher</span></span>
<span data-ttu-id="d006a-123">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="d006a-123">The network watcher resource.</span></span>

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

### <span data-ttu-id="d006a-124">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d006a-124">-NetworkWatcherName</span></span>
<span data-ttu-id="d006a-125">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="d006a-125">The name of network watcher.</span></span>

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

### <span data-ttu-id="d006a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d006a-126">-ResourceGroupName</span></span>
<span data-ttu-id="d006a-127">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="d006a-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d006a-128">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="d006a-128">-TargetResourceId</span></span>
<span data-ttu-id="d006a-129">Die Ziel Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="d006a-129">The target resource ID.</span></span>

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

### <span data-ttu-id="d006a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d006a-130">CommonParameters</span></span>
<span data-ttu-id="d006a-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d006a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d006a-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d006a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d006a-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d006a-133">INPUTS</span></span>

### <span data-ttu-id="d006a-134">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d006a-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="d006a-135">Parameter: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d006a-135">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="d006a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d006a-136">System.String</span></span>
<span data-ttu-id="d006a-137">Parameter: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d006a-137">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="d006a-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d006a-138">OUTPUTS</span></span>

### <span data-ttu-id="d006a-139">Microsoft. Azure. Commands. Network. Models. PSTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="d006a-139">Microsoft.Azure.Commands.Network.Models.PSTroubleshootingResult</span></span>

## <span data-ttu-id="d006a-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="d006a-140">NOTES</span></span>
<span data-ttu-id="d006a-141">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerkmonitor, Problembehandlung, VPN, Verbindung</span><span class="sxs-lookup"><span data-stu-id="d006a-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, troubleshoot, VPN, connection</span></span>

## <span data-ttu-id="d006a-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d006a-142">RELATED LINKS</span></span>

[<span data-ttu-id="d006a-143">Neu – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d006a-143">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="d006a-144">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d006a-144">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="d006a-145">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d006a-145">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="d006a-146">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d006a-146">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="d006a-147">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d006a-147">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d006a-148">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d006a-148">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="d006a-149">Anfang-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d006a-149">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="d006a-150">Neu – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d006a-150">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d006a-151">Neu – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d006a-151">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="d006a-152">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d006a-152">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d006a-153">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d006a-153">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d006a-154">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d006a-154">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d006a-155">Neu – AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="d006a-155">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="d006a-156">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d006a-156">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="d006a-157">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="d006a-157">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="d006a-158">Stopp-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d006a-158">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d006a-159">Anfang-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d006a-159">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d006a-160">Satz-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d006a-160">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d006a-161">Satz-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="d006a-161">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="d006a-162">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d006a-162">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d006a-163">Neu – AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d006a-163">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d006a-164">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="d006a-164">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="d006a-165">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="d006a-165">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="d006a-166">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="d006a-166">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="d006a-167">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="d006a-167">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="d006a-168">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="d006a-168">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="d006a-169">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d006a-169">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
