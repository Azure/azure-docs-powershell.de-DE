---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: f6762b074c9b185d12666fb8ea92fcaf15a46b05
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98292486"
---
# <span data-ttu-id="5fc25-101">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5fc25-101">New-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="5fc25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fc25-102">SYNOPSIS</span></span>
<span data-ttu-id="5fc25-103">Erstellt eine neue Paketaufnahmeressource und startet eine Paketaufnahmesitzung auf einer VM.</span><span class="sxs-lookup"><span data-stu-id="5fc25-103">Creates a new packet capture resource and starts a packet capture session on a VM.</span></span>

## <span data-ttu-id="5fc25-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5fc25-104">SYNTAX</span></span>

### <span data-ttu-id="5fc25-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="5fc25-105">SetByResource (Default)</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fc25-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="5fc25-106">SetByName</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> -TargetVirtualMachineId <String> [-StorageAccountId <String>]
 [-StoragePath <String>] [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>]
 [-TotalBytesPerSession <Int32>] [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fc25-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="5fc25-107">SetByLocation</span></span>
```
New-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fc25-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5fc25-108">DESCRIPTION</span></span>
<span data-ttu-id="5fc25-109">Das New-AzNetworkWatcherPacketCapture cmdlet erstellt eine neue Paketaufnahmeressource und startet eine Paketaufnahmesitzung auf einer VM.</span><span class="sxs-lookup"><span data-stu-id="5fc25-109">The New-AzNetworkWatcherPacketCapture cmdlet creates a new packet capture resource and starts a packet capture session on a VM.</span></span>
<span data-ttu-id="5fc25-110">Die Länge der Paketerfassungssitzungen kann über eine Zeiteinschränkung oder größenbeschränkung konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="5fc25-110">The length of the Packet Capture sessions can be configured via a time constraint or a size constraint.</span></span> <span data-ttu-id="5fc25-111">Die Menge der für jedes Paket erfassten Daten kann ebenfalls konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="5fc25-111">The amount of data captured for each packet can also be configured.</span></span>
<span data-ttu-id="5fc25-112">Filter können auf eine bestimmte Paketaufnahmesitzung angewendet werden, sodass Sie die Art der aufgenommenen Pakete anpassen können.</span><span class="sxs-lookup"><span data-stu-id="5fc25-112">Filters can be applied to a given packet capture session, allowing you to customize the type of packets captured.</span></span> <span data-ttu-id="5fc25-113">Filter können Pakete für lokale und Remote-IP-Adressen & Adressbereichen, lokale Ports und Remoteports & Portbereichen und das zu erfassende Protokoll auf Sitzungsebene einschränken.</span><span class="sxs-lookup"><span data-stu-id="5fc25-113">Filters can restrict packets on local and remote IP addresses & address ranges, local and remote ports & port ranges, and the session level protocol to be captured.</span></span> <span data-ttu-id="5fc25-114">Filter können zusammensetzbar sein, und es können mehrere Filter angewendet werden, um die Granularität der Aufnahme zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="5fc25-114">Filters are composable, and multiple filters can be applied to provide you with granularity of capture.</span></span>

## <span data-ttu-id="5fc25-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5fc25-115">EXAMPLES</span></span>

### <span data-ttu-id="5fc25-116">Beispiel 1: Erstellen einer Paketaufzeichnung mit mehreren Filtern</span><span class="sxs-lookup"><span data-stu-id="5fc25-116">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filter $filter1, $filter2
```

<span data-ttu-id="5fc25-117">In diesem Beispiel erstellen wir eine Paketaufzeichnung namens "PacketCaptureTest" mit mehreren Filtern und einem Zeitlimit.</span><span class="sxs-lookup"><span data-stu-id="5fc25-117">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="5fc25-118">Nach Abschluss der Sitzung wird sie im angegebenen Speicherkonto gespeichert.</span><span class="sxs-lookup"><span data-stu-id="5fc25-118">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="5fc25-119">Hinweis: Die Azure Network Watcher-Erweiterung muss auf dem virtuellen Zielcomputer installiert sein, um Paketaufzeichnungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5fc25-119">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="5fc25-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5fc25-120">PARAMETERS</span></span>

### <span data-ttu-id="5fc25-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5fc25-121">-AsJob</span></span>
<span data-ttu-id="5fc25-122">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5fc25-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5fc25-123">-BytesToCapturePerPacket</span><span class="sxs-lookup"><span data-stu-id="5fc25-123">-BytesToCapturePerPacket</span></span>
<span data-ttu-id="5fc25-124">Bytes, die pro Paket erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="5fc25-124">Bytes to capture per packet.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fc25-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fc25-125">-DefaultProfile</span></span>
<span data-ttu-id="5fc25-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5fc25-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5fc25-127">-Filter</span><span class="sxs-lookup"><span data-stu-id="5fc25-127">-Filter</span></span>
<span data-ttu-id="5fc25-128">Filter für die Paketaufnahmesitzung.</span><span class="sxs-lookup"><span data-stu-id="5fc25-128">Filters for packet capture session.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fc25-129">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="5fc25-129">-LocalFilePath</span></span>
<span data-ttu-id="5fc25-130">Lokaler Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="5fc25-130">Local file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fc25-131">-Location</span><span class="sxs-lookup"><span data-stu-id="5fc25-131">-Location</span></span>
<span data-ttu-id="5fc25-132">Position der Netzwerk-Watcher.</span><span class="sxs-lookup"><span data-stu-id="5fc25-132">Location of the network watcher.</span></span>

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

### <span data-ttu-id="5fc25-133">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5fc25-133">-NetworkWatcher</span></span>
<span data-ttu-id="5fc25-134">Die Netzwerk-Watcher-Ressource.</span><span class="sxs-lookup"><span data-stu-id="5fc25-134">The network watcher resource.</span></span>

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

### <span data-ttu-id="5fc25-135">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="5fc25-135">-NetworkWatcherName</span></span>
<span data-ttu-id="5fc25-136">Der Name der Netzwerk-Watcher.</span><span class="sxs-lookup"><span data-stu-id="5fc25-136">The name of network watcher.</span></span>

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

### <span data-ttu-id="5fc25-137">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="5fc25-137">-PacketCaptureName</span></span>
<span data-ttu-id="5fc25-138">Der Name der Paketaufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="5fc25-138">The packet capture name.</span></span>

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

### <span data-ttu-id="5fc25-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fc25-139">-ResourceGroupName</span></span>
<span data-ttu-id="5fc25-140">Der Name der Ressourcengruppe "Netzwerk-Watcher".</span><span class="sxs-lookup"><span data-stu-id="5fc25-140">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="5fc25-141">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="5fc25-141">-StorageAccountId</span></span>
<span data-ttu-id="5fc25-142">Speicherkonto-ID.</span><span class="sxs-lookup"><span data-stu-id="5fc25-142">Storage account Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fc25-143">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="5fc25-143">-StoragePath</span></span>
<span data-ttu-id="5fc25-144">Speicherpfad.</span><span class="sxs-lookup"><span data-stu-id="5fc25-144">Storage path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fc25-145">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="5fc25-145">-TargetVirtualMachineId</span></span>
<span data-ttu-id="5fc25-146">Die Ziel-ID des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="5fc25-146">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="5fc25-147">-TimeLimitInSeconds</span><span class="sxs-lookup"><span data-stu-id="5fc25-147">-TimeLimitInSeconds</span></span>
<span data-ttu-id="5fc25-148">Zeitlimit in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="5fc25-148">Time limit in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fc25-149">-TotalBytesPerSession</span><span class="sxs-lookup"><span data-stu-id="5fc25-149">-TotalBytesPerSession</span></span>
<span data-ttu-id="5fc25-150">Gesamtzahl der Bytes pro Sitzung.</span><span class="sxs-lookup"><span data-stu-id="5fc25-150">Total bytes per session.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fc25-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5fc25-151">-Confirm</span></span>
<span data-ttu-id="5fc25-152">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5fc25-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fc25-153">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5fc25-153">-WhatIf</span></span>
<span data-ttu-id="5fc25-154">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5fc25-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fc25-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5fc25-155">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fc25-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fc25-156">CommonParameters</span></span>
<span data-ttu-id="5fc25-157">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fc25-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fc25-158">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fc25-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fc25-159">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5fc25-159">INPUTS</span></span>

### <span data-ttu-id="5fc25-160">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5fc25-160">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="5fc25-161">System.String</span><span class="sxs-lookup"><span data-stu-id="5fc25-161">System.String</span></span>

### <span data-ttu-id="5fc25-162">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5fc25-162">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="5fc25-163">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5fc25-163">OUTPUTS</span></span>

### <span data-ttu-id="5fc25-164">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="5fc25-164">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureResult</span></span>

## <span data-ttu-id="5fc25-165">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5fc25-165">NOTES</span></span>
<span data-ttu-id="5fc25-166">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span><span class="sxs-lookup"><span data-stu-id="5fc25-166">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span> 

## <span data-ttu-id="5fc25-167">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5fc25-167">RELATED LINKS</span></span>

[<span data-ttu-id="5fc25-168">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5fc25-168">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="5fc25-169">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5fc25-169">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="5fc25-170">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5fc25-170">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="5fc25-171">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="5fc25-171">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="5fc25-172">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="5fc25-172">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="5fc25-173">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="5fc25-173">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="5fc25-174">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="5fc25-174">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="5fc25-175">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5fc25-175">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5fc25-176">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="5fc25-176">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="5fc25-177">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5fc25-177">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5fc25-178">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5fc25-178">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5fc25-179">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5fc25-179">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5fc25-180">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="5fc25-180">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="5fc25-181">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="5fc25-181">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="5fc25-182">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="5fc25-182">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="5fc25-183">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5fc25-183">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5fc25-184">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5fc25-184">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5fc25-185">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5fc25-185">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5fc25-186">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="5fc25-186">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="5fc25-187">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5fc25-187">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5fc25-188">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5fc25-188">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5fc25-189">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="5fc25-189">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="5fc25-190">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="5fc25-190">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="5fc25-191">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="5fc25-191">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="5fc25-192">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="5fc25-192">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="5fc25-193">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="5fc25-193">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="5fc25-194">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5fc25-194">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)


