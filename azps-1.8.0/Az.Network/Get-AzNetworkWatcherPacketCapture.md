---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 94d59f66563e3d4fd5f236613676e0cbe6b466c8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660728"
---
# <span data-ttu-id="d74fa-101">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d74fa-101">Get-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="d74fa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d74fa-102">SYNOPSIS</span></span>
<span data-ttu-id="d74fa-103">Ruft Informationen und Eigenschaften sowie den Status einer Paket Erfassungs Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="d74fa-103">Gets information and properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="d74fa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d74fa-104">SYNTAX</span></span>

### <span data-ttu-id="d74fa-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="d74fa-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d74fa-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="d74fa-106">SetByName</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d74fa-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="d74fa-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherPacketCapture -Location <String> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d74fa-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d74fa-108">DESCRIPTION</span></span>
<span data-ttu-id="d74fa-109">Die Get-AzNetworkWatcherPacketCapture ruft die Eigenschaften und den Status einer Paket Erfassungs Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="d74fa-109">The Get-AzNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="d74fa-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d74fa-110">EXAMPLES</span></span>

### <span data-ttu-id="d74fa-111">Beispiel 1: Erstellen einer Paketerfassung mit mehreren Filtern und Abrufen des Status</span><span class="sxs-lookup"><span data-stu-id="d74fa-111">Example 1: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="d74fa-112">In diesem Beispiel erstellen wir eine Paketerfassung mit dem Namen "PacketCaptureTest" mit mehreren Filtern und einem Zeitlimit.</span><span class="sxs-lookup"><span data-stu-id="d74fa-112">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="d74fa-113">Nachdem die Sitzung abgeschlossen ist, wird Sie im angegebenen Speicherkonto gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d74fa-113">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="d74fa-114">Anschließend rufen wir Get-AzNetworkWatcherPacketCapture auf, um den Status der Aufnahmesitzung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d74fa-114">We then call Get-AzNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> <span data-ttu-id="d74fa-115">Hinweis: die Azure Network Watcher-Erweiterung muss auf dem virtuellen Zielcomputer installiert sein, um Paketerfassungen erstellen zu können.</span><span class="sxs-lookup"><span data-stu-id="d74fa-115">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

### <span data-ttu-id="d74fa-116">Beispiel 2: Erstellen einer Paketerfassung mit mehreren Filtern und Abrufen des Status</span><span class="sxs-lookup"><span data-stu-id="d74fa-116">Example 2: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
Get-AzNetworkWatcherPacketCapture -ResourceGroupName rg1 -NetworkWatcherName nw1 -PacketCaptureName PacketCapture*
```

<span data-ttu-id="d74fa-117">Dieses Cmdlet gibt alle PacketCaptures zurück, die mit "PacketCapture" im NW1-Netzwerkmonitor beginnen.</span><span class="sxs-lookup"><span data-stu-id="d74fa-117">This cmdlet returns all PacketCaptures that start with "PacketCapture" in the nw1 Network Watcher.</span></span>

## <span data-ttu-id="d74fa-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="d74fa-118">PARAMETERS</span></span>

### <span data-ttu-id="d74fa-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d74fa-119">-AsJob</span></span>
<span data-ttu-id="d74fa-120">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d74fa-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d74fa-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d74fa-121">-DefaultProfile</span></span>
<span data-ttu-id="d74fa-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d74fa-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d74fa-123">-Standort</span><span class="sxs-lookup"><span data-stu-id="d74fa-123">-Location</span></span>
<span data-ttu-id="d74fa-124">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="d74fa-124">Location of the network watcher.</span></span>

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

### <span data-ttu-id="d74fa-125">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d74fa-125">-NetworkWatcher</span></span>
<span data-ttu-id="d74fa-126">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="d74fa-126">The network watcher resource.</span></span>

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

### <span data-ttu-id="d74fa-127">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d74fa-127">-NetworkWatcherName</span></span>
<span data-ttu-id="d74fa-128">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="d74fa-128">The name of network watcher.</span></span>

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

### <span data-ttu-id="d74fa-129">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="d74fa-129">-PacketCaptureName</span></span>
<span data-ttu-id="d74fa-130">Der Name der Paketaufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="d74fa-130">The packet capture name.</span></span>

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

### <span data-ttu-id="d74fa-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d74fa-131">-ResourceGroupName</span></span>
<span data-ttu-id="d74fa-132">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="d74fa-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d74fa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d74fa-133">CommonParameters</span></span>
<span data-ttu-id="d74fa-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d74fa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d74fa-135">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d74fa-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d74fa-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d74fa-136">INPUTS</span></span>

### <span data-ttu-id="d74fa-137">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d74fa-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="d74fa-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d74fa-138">System.String</span></span>

## <span data-ttu-id="d74fa-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d74fa-139">OUTPUTS</span></span>

### <span data-ttu-id="d74fa-140">Microsoft. Azure. Commands. Network. Models. PSGetPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="d74fa-140">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="d74fa-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="d74fa-141">NOTES</span></span>
<span data-ttu-id="d74fa-142">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerk Watcher, Paket, Capture, Traffic</span><span class="sxs-lookup"><span data-stu-id="d74fa-142">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="d74fa-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d74fa-143">RELATED LINKS</span></span>

[<span data-ttu-id="d74fa-144">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d74fa-144">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="d74fa-145">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d74fa-145">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="d74fa-146">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d74fa-146">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="d74fa-147">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d74fa-147">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="d74fa-148">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d74fa-148">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d74fa-149">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d74fa-149">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="d74fa-150">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d74fa-150">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="d74fa-151">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d74fa-151">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d74fa-152">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d74fa-152">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="d74fa-153">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d74fa-153">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d74fa-154">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d74fa-154">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d74fa-155">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d74fa-155">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d74fa-156">Neu – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="d74fa-156">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="d74fa-157">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d74fa-157">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="d74fa-158">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="d74fa-158">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="d74fa-159">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d74fa-159">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d74fa-160">Anfang-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d74fa-160">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d74fa-161">Satz-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d74fa-161">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d74fa-162">Satz-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="d74fa-162">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="d74fa-163">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d74fa-163">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d74fa-164">Neu – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d74fa-164">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d74fa-165">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="d74fa-165">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="d74fa-166">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="d74fa-166">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="d74fa-167">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="d74fa-167">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="d74fa-168">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="d74fa-168">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="d74fa-169">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="d74fa-169">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="d74fa-170">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d74fa-170">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

