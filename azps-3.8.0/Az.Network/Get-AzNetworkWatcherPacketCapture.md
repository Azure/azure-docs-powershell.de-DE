---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: e836bb8738b594e09c65568cc0f454a476db9d34
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100408881"
---
# <span data-ttu-id="16f3c-101">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="16f3c-101">Get-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="16f3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16f3c-102">SYNOPSIS</span></span>
<span data-ttu-id="16f3c-103">Ruft Informationen und Eigenschaften sowie den Status einer Paketaufnahmeressource ab.</span><span class="sxs-lookup"><span data-stu-id="16f3c-103">Gets information and properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="16f3c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="16f3c-104">SYNTAX</span></span>

### <span data-ttu-id="16f3c-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="16f3c-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16f3c-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="16f3c-106">SetByName</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16f3c-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="16f3c-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherPacketCapture -Location <String> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16f3c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="16f3c-108">DESCRIPTION</span></span>
<span data-ttu-id="16f3c-109">Die Get-AzNetworkWatcherPacketCapture ruft die Eigenschaften und den Status einer Paketaufnahmeressource ab.</span><span class="sxs-lookup"><span data-stu-id="16f3c-109">The Get-AzNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="16f3c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="16f3c-110">EXAMPLES</span></span>

### <span data-ttu-id="16f3c-111">Beispiel 1: Erstellen einer Paketaufzeichnung mit mehreren Filtern und Abrufen des Status</span><span class="sxs-lookup"><span data-stu-id="16f3c-111">Example 1: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="16f3c-112">In diesem Beispiel erstellen wir eine Paketaufzeichnung namens "PacketCaptureTest" mit mehreren Filtern und einem Zeitlimit.</span><span class="sxs-lookup"><span data-stu-id="16f3c-112">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="16f3c-113">Nach Abschluss der Sitzung wird sie im angegebenen Speicherkonto gespeichert.</span><span class="sxs-lookup"><span data-stu-id="16f3c-113">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="16f3c-114">Anschließend rufen wir Get-AzNetworkWatcherPacketCapture, um den Status der Aufnahmesitzung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="16f3c-114">We then call Get-AzNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> <span data-ttu-id="16f3c-115">Hinweis: Die Azure Network Watcher-Erweiterung muss auf dem virtuellen Zielcomputer installiert sein, um Paketaufzeichnungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="16f3c-115">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

>[!NOTE]
><span data-ttu-id="16f3c-116">Wenn Sie einen Verweis auf die Paketaufnahme direkt über den Befehl New-AzNetworkWatcherPacketCapture erstellen, besitzt er nicht alle Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="16f3c-116">If you create a reference to the packet capture directly from the New-AzNetworkWatcherPacketCapture command, it won't have all the properties.</span></span> <span data-ttu-id="16f3c-117">Sie können alle Eigenschaften der Paketaufnahme erhalten, indem Sie einen Aufruf des Befehls Get-AzNetworkWatcherPacketCapture ausführen.</span><span class="sxs-lookup"><span data-stu-id="16f3c-117">You can get all of the properties of the packet capture by making a call to the Get-AzNetworkWatcherPacketCapture command.</span></span>

### <span data-ttu-id="16f3c-118">Beispiel 2: Erstellen einer Paketaufzeichnung mit mehreren Filtern und Abrufen des Status</span><span class="sxs-lookup"><span data-stu-id="16f3c-118">Example 2: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
Get-AzNetworkWatcherPacketCapture -ResourceGroupName rg1 -NetworkWatcherName nw1 -PacketCaptureName PacketCapture*
```

<span data-ttu-id="16f3c-119">Dieses Cmdlet gibt alle PacketCaptures zurück, die mit "PacketCapture" im nw1 Network Watcher beginnen.</span><span class="sxs-lookup"><span data-stu-id="16f3c-119">This cmdlet returns all PacketCaptures that start with "PacketCapture" in the nw1 Network Watcher.</span></span>

## <span data-ttu-id="16f3c-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16f3c-120">PARAMETERS</span></span>

### <span data-ttu-id="16f3c-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="16f3c-121">-AsJob</span></span>
<span data-ttu-id="16f3c-122">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="16f3c-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="16f3c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16f3c-123">-DefaultProfile</span></span>
<span data-ttu-id="16f3c-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="16f3c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16f3c-125">-Location</span><span class="sxs-lookup"><span data-stu-id="16f3c-125">-Location</span></span>
<span data-ttu-id="16f3c-126">Speicherort der Netzwerk-Watcher.</span><span class="sxs-lookup"><span data-stu-id="16f3c-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="16f3c-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="16f3c-127">-NetworkWatcher</span></span>
<span data-ttu-id="16f3c-128">Die Netzwerk-Watcher-Ressource.</span><span class="sxs-lookup"><span data-stu-id="16f3c-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="16f3c-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="16f3c-129">-NetworkWatcherName</span></span>
<span data-ttu-id="16f3c-130">Der Name der Netzwerk-Watcher.</span><span class="sxs-lookup"><span data-stu-id="16f3c-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="16f3c-131">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="16f3c-131">-PacketCaptureName</span></span>
<span data-ttu-id="16f3c-132">Der Name der Paketaufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="16f3c-132">The packet capture name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="16f3c-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16f3c-133">-ResourceGroupName</span></span>
<span data-ttu-id="16f3c-134">Der Name der Ressourcengruppe "Netzwerk-Watcher".</span><span class="sxs-lookup"><span data-stu-id="16f3c-134">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="16f3c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16f3c-135">CommonParameters</span></span>
<span data-ttu-id="16f3c-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16f3c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16f3c-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16f3c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16f3c-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="16f3c-138">INPUTS</span></span>

### <span data-ttu-id="16f3c-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="16f3c-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="16f3c-140">System.String</span><span class="sxs-lookup"><span data-stu-id="16f3c-140">System.String</span></span>

## <span data-ttu-id="16f3c-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="16f3c-141">OUTPUTS</span></span>

### <span data-ttu-id="16f3c-142">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="16f3c-142">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="16f3c-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="16f3c-143">NOTES</span></span>
<span data-ttu-id="16f3c-144">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span><span class="sxs-lookup"><span data-stu-id="16f3c-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="16f3c-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="16f3c-145">RELATED LINKS</span></span>

[<span data-ttu-id="16f3c-146">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="16f3c-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="16f3c-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="16f3c-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="16f3c-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="16f3c-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="16f3c-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="16f3c-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="16f3c-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="16f3c-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="16f3c-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="16f3c-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="16f3c-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="16f3c-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="16f3c-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="16f3c-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="16f3c-154">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="16f3c-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="16f3c-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="16f3c-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="16f3c-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="16f3c-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="16f3c-157">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="16f3c-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="16f3c-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="16f3c-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="16f3c-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="16f3c-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="16f3c-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="16f3c-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="16f3c-161">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="16f3c-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="16f3c-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="16f3c-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="16f3c-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="16f3c-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="16f3c-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="16f3c-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="16f3c-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="16f3c-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="16f3c-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="16f3c-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="16f3c-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="16f3c-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="16f3c-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="16f3c-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="16f3c-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="16f3c-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="16f3c-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="16f3c-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="16f3c-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="16f3c-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="16f3c-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="16f3c-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

