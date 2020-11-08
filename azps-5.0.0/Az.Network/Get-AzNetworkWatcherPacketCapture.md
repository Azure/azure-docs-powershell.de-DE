---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 1276a3c63ec4b9c4ec1c2c4c91ea792013cbacc9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178788"
---
# <span data-ttu-id="1511b-101">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1511b-101">Get-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="1511b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1511b-102">SYNOPSIS</span></span>
<span data-ttu-id="1511b-103">Ruft Informationen und Eigenschaften sowie den Status einer Paket Erfassungs Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="1511b-103">Gets information and properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="1511b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1511b-104">SYNTAX</span></span>

### <span data-ttu-id="1511b-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="1511b-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1511b-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="1511b-106">SetByName</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1511b-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="1511b-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherPacketCapture -Location <String> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1511b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1511b-108">DESCRIPTION</span></span>
<span data-ttu-id="1511b-109">Die Get-AzNetworkWatcherPacketCapture ruft die Eigenschaften und den Status einer Paket Erfassungs Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="1511b-109">The Get-AzNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="1511b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1511b-110">EXAMPLES</span></span>

### <span data-ttu-id="1511b-111">Beispiel 1: Erstellen einer Paketerfassung mit mehreren Filtern und Abrufen des Status</span><span class="sxs-lookup"><span data-stu-id="1511b-111">Example 1: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="1511b-112">In diesem Beispiel erstellen wir eine Paketerfassung mit dem Namen "PacketCaptureTest" mit mehreren Filtern und einem Zeitlimit.</span><span class="sxs-lookup"><span data-stu-id="1511b-112">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="1511b-113">Nachdem die Sitzung abgeschlossen ist, wird Sie im angegebenen Speicherkonto gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1511b-113">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="1511b-114">Anschließend rufen wir Get-AzNetworkWatcherPacketCapture auf, um den Status der Aufnahmesitzung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1511b-114">We then call Get-AzNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> <span data-ttu-id="1511b-115">Hinweis: die Azure Network Watcher-Erweiterung muss auf dem virtuellen Zielcomputer installiert sein, um Paketerfassungen erstellen zu können.</span><span class="sxs-lookup"><span data-stu-id="1511b-115">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

>[!NOTE]
><span data-ttu-id="1511b-116">Wenn Sie einen Verweis auf die Paketerfassung direkt über den Befehl New-AzNetworkWatcherPacketCapture erstellen, verfügen Sie nicht über alle Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1511b-116">If you create a reference to the packet capture directly from the New-AzNetworkWatcherPacketCapture command, it won't have all the properties.</span></span> <span data-ttu-id="1511b-117">Sie können alle Eigenschaften der Paketerfassung abrufen, indem Sie den Befehl Get-AzNetworkWatcherPacketCapture aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1511b-117">You can get all of the properties of the packet capture by making a call to the Get-AzNetworkWatcherPacketCapture command.</span></span>

### <span data-ttu-id="1511b-118">Beispiel 2: Erstellen einer Paketerfassung mit mehreren Filtern und Abrufen des Status</span><span class="sxs-lookup"><span data-stu-id="1511b-118">Example 2: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
Get-AzNetworkWatcherPacketCapture -ResourceGroupName rg1 -NetworkWatcherName nw1 -PacketCaptureName PacketCapture*
```

<span data-ttu-id="1511b-119">Dieses Cmdlet gibt alle PacketCaptures zurück, die mit "PacketCapture" im NW1-Netzwerkmonitor beginnen.</span><span class="sxs-lookup"><span data-stu-id="1511b-119">This cmdlet returns all PacketCaptures that start with "PacketCapture" in the nw1 Network Watcher.</span></span>

## <span data-ttu-id="1511b-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="1511b-120">PARAMETERS</span></span>

### <span data-ttu-id="1511b-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1511b-121">-AsJob</span></span>
<span data-ttu-id="1511b-122">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1511b-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1511b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1511b-123">-DefaultProfile</span></span>
<span data-ttu-id="1511b-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1511b-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1511b-125">-Standort</span><span class="sxs-lookup"><span data-stu-id="1511b-125">-Location</span></span>
<span data-ttu-id="1511b-126">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="1511b-126">Location of the network watcher.</span></span>

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

### <span data-ttu-id="1511b-127">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1511b-127">-NetworkWatcher</span></span>
<span data-ttu-id="1511b-128">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="1511b-128">The network watcher resource.</span></span>

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

### <span data-ttu-id="1511b-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="1511b-129">-NetworkWatcherName</span></span>
<span data-ttu-id="1511b-130">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="1511b-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="1511b-131">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="1511b-131">-PacketCaptureName</span></span>
<span data-ttu-id="1511b-132">Der Name der Paketaufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="1511b-132">The packet capture name.</span></span>

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

### <span data-ttu-id="1511b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1511b-133">-ResourceGroupName</span></span>
<span data-ttu-id="1511b-134">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="1511b-134">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="1511b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1511b-135">CommonParameters</span></span>
<span data-ttu-id="1511b-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1511b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1511b-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1511b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1511b-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1511b-138">INPUTS</span></span>

### <span data-ttu-id="1511b-139">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1511b-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="1511b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="1511b-140">System.String</span></span>

## <span data-ttu-id="1511b-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1511b-141">OUTPUTS</span></span>

### <span data-ttu-id="1511b-142">Microsoft. Azure. Commands. Network. Models. PSGetPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="1511b-142">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="1511b-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="1511b-143">NOTES</span></span>
<span data-ttu-id="1511b-144">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerk Watcher, Paket, Capture, Traffic</span><span class="sxs-lookup"><span data-stu-id="1511b-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="1511b-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1511b-145">RELATED LINKS</span></span>

[<span data-ttu-id="1511b-146">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1511b-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="1511b-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1511b-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="1511b-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1511b-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="1511b-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="1511b-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="1511b-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="1511b-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="1511b-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="1511b-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="1511b-152">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="1511b-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="1511b-153">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1511b-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1511b-154">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="1511b-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="1511b-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1511b-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1511b-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1511b-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1511b-157">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1511b-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1511b-158">Neu – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="1511b-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="1511b-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="1511b-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="1511b-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="1511b-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="1511b-161">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1511b-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1511b-162">Anfang-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1511b-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1511b-163">Satz-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1511b-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1511b-164">Satz-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="1511b-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="1511b-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1511b-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1511b-166">Neu – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1511b-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1511b-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="1511b-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="1511b-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="1511b-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="1511b-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="1511b-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="1511b-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="1511b-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="1511b-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="1511b-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="1511b-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1511b-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

