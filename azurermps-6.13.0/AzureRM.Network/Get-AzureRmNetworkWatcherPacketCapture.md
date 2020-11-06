---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 00adf4abd887c56f4091761a4a2031bb6b033032
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503549"
---
# <span data-ttu-id="cd8ef-101">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cd8ef-101">Get-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="cd8ef-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cd8ef-102">SYNOPSIS</span></span>
<span data-ttu-id="cd8ef-103">Ruft Informationen und Eigenschaften sowie den Status einer Paket Erfassungs Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="cd8ef-103">Gets information and properties and status of a packet capture resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd8ef-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd8ef-104">SYNTAX</span></span>

### <span data-ttu-id="cd8ef-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="cd8ef-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd8ef-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="cd8ef-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd8ef-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="cd8ef-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -Location <String> [-PacketCaptureName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd8ef-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cd8ef-108">DESCRIPTION</span></span>
<span data-ttu-id="cd8ef-109">Die Get-AzureRmNetworkWatcherPacketCapture ruft die Eigenschaften und den Status einer Paket Erfassungs Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="cd8ef-109">The Get-AzureRmNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="cd8ef-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cd8ef-110">EXAMPLES</span></span>

### <span data-ttu-id="cd8ef-111">Beispiel 1: Erstellen einer Paketerfassung mit mehreren Filtern und Abrufen des Status</span><span class="sxs-lookup"><span data-stu-id="cd8ef-111">Example 1: Create a Packet Capture with multiple filters and retrieve its status</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="cd8ef-112">In diesem Beispiel erstellen wir eine Paketerfassung mit dem Namen "PacketCaptureTest" mit mehreren Filtern und einem Zeitlimit.</span><span class="sxs-lookup"><span data-stu-id="cd8ef-112">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="cd8ef-113">Nachdem die Sitzung abgeschlossen ist, wird Sie im angegebenen Speicherkonto gespeichert.</span><span class="sxs-lookup"><span data-stu-id="cd8ef-113">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="cd8ef-114">Anschließend rufen wir Get-AzureRmNetworkWatcherPacketCapture auf, um den Status der Aufnahmesitzung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="cd8ef-114">We then call Get-AzureRmNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> <span data-ttu-id="cd8ef-115">Hinweis: die Azure Network Watcher-Erweiterung muss auf dem virtuellen Zielcomputer installiert sein, um Paketerfassungen erstellen zu können.</span><span class="sxs-lookup"><span data-stu-id="cd8ef-115">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="cd8ef-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd8ef-116">PARAMETERS</span></span>

### <span data-ttu-id="cd8ef-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd8ef-117">-AsJob</span></span>
<span data-ttu-id="cd8ef-118">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="cd8ef-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd8ef-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd8ef-119">-DefaultProfile</span></span>
<span data-ttu-id="cd8ef-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cd8ef-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd8ef-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="cd8ef-121">-Location</span></span>
<span data-ttu-id="cd8ef-122">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="cd8ef-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="cd8ef-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cd8ef-123">-NetworkWatcher</span></span>
<span data-ttu-id="cd8ef-124">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="cd8ef-124">The network watcher resource.</span></span>

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

### <span data-ttu-id="cd8ef-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="cd8ef-125">-NetworkWatcherName</span></span>
<span data-ttu-id="cd8ef-126">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="cd8ef-126">The name of network watcher.</span></span>

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

### <span data-ttu-id="cd8ef-127">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="cd8ef-127">-PacketCaptureName</span></span>
<span data-ttu-id="cd8ef-128">Der Name der Paketaufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="cd8ef-128">The packet capture name.</span></span>

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

### <span data-ttu-id="cd8ef-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd8ef-129">-ResourceGroupName</span></span>
<span data-ttu-id="cd8ef-130">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="cd8ef-130">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="cd8ef-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd8ef-131">CommonParameters</span></span>
<span data-ttu-id="cd8ef-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd8ef-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd8ef-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd8ef-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd8ef-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cd8ef-134">INPUTS</span></span>

### <span data-ttu-id="cd8ef-135">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cd8ef-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="cd8ef-136">Parameter: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cd8ef-136">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="cd8ef-137">System. String</span><span class="sxs-lookup"><span data-stu-id="cd8ef-137">System.String</span></span>
<span data-ttu-id="cd8ef-138">Parameter: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cd8ef-138">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="cd8ef-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cd8ef-139">OUTPUTS</span></span>

### <span data-ttu-id="cd8ef-140">Microsoft. Azure. Commands. Network. Models. PSGetPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="cd8ef-140">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="cd8ef-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="cd8ef-141">NOTES</span></span>
<span data-ttu-id="cd8ef-142">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerk Watcher, Paket, Capture, Traffic</span><span class="sxs-lookup"><span data-stu-id="cd8ef-142">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="cd8ef-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cd8ef-143">RELATED LINKS</span></span>

[<span data-ttu-id="cd8ef-144">Neu – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cd8ef-144">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="cd8ef-145">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cd8ef-145">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="cd8ef-146">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cd8ef-146">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="cd8ef-147">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="cd8ef-147">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="cd8ef-148">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="cd8ef-148">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="cd8ef-149">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="cd8ef-149">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="cd8ef-150">Anfang-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="cd8ef-150">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="cd8ef-151">Neu – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cd8ef-151">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cd8ef-152">Neu – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="cd8ef-152">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="cd8ef-153">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cd8ef-153">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cd8ef-154">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cd8ef-154">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cd8ef-155">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cd8ef-155">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cd8ef-156">Neu – AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd8ef-156">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="cd8ef-157">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="cd8ef-157">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="cd8ef-158">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="cd8ef-158">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="cd8ef-159">Stopp-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cd8ef-159">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cd8ef-160">Anfang-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cd8ef-160">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cd8ef-161">Satz-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cd8ef-161">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cd8ef-162">Satz-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="cd8ef-162">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="cd8ef-163">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cd8ef-163">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cd8ef-164">Neu – AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cd8ef-164">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cd8ef-165">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="cd8ef-165">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="cd8ef-166">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="cd8ef-166">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="cd8ef-167">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="cd8ef-167">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="cd8ef-168">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="cd8ef-168">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="cd8ef-169">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="cd8ef-169">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="cd8ef-170">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cd8ef-170">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)

