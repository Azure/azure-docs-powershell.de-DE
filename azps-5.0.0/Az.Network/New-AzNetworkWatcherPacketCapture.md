---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: f6762b074c9b185d12666fb8ea92fcaf15a46b05
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178323"
---
# <span data-ttu-id="1b925-101">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1b925-101">New-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="1b925-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1b925-102">SYNOPSIS</span></span>
<span data-ttu-id="1b925-103">Erstellt eine neue Paket Erfassungs Ressource und startet eine Paket Aufnahmesitzung auf einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="1b925-103">Creates a new packet capture resource and starts a packet capture session on a VM.</span></span>

## <span data-ttu-id="1b925-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b925-104">SYNTAX</span></span>

### <span data-ttu-id="1b925-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="1b925-105">SetByResource (Default)</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b925-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="1b925-106">SetByName</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> -TargetVirtualMachineId <String> [-StorageAccountId <String>]
 [-StoragePath <String>] [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>]
 [-TotalBytesPerSession <Int32>] [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b925-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="1b925-107">SetByLocation</span></span>
```
New-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b925-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1b925-108">DESCRIPTION</span></span>
<span data-ttu-id="1b925-109">Das New-AzNetworkWatcherPacketCapture-Cmdlet erstellt eine neue Paket Erfassungs Ressource und startet eine Paket Aufnahmesitzung auf einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="1b925-109">The New-AzNetworkWatcherPacketCapture cmdlet creates a new packet capture resource and starts a packet capture session on a VM.</span></span>
<span data-ttu-id="1b925-110">Die Länge der Paket Aufnahmesitzungen kann über eine Zeitbeschränkung oder eine Größenbeschränkung konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="1b925-110">The length of the Packet Capture sessions can be configured via a time constraint or a size constraint.</span></span> <span data-ttu-id="1b925-111">Die für die einzelnen Pakete erfassten Datenmengen können ebenfalls konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="1b925-111">The amount of data captured for each packet can also be configured.</span></span>
<span data-ttu-id="1b925-112">Filter können auf eine bestimmte Paket Aufnahmesitzung angewendet werden, sodass Sie den Typ der erfassten Pakete anpassen können.</span><span class="sxs-lookup"><span data-stu-id="1b925-112">Filters can be applied to a given packet capture session, allowing you to customize the type of packets captured.</span></span> <span data-ttu-id="1b925-113">Filter können Pakete für lokale und Remote-IP-Adressen einschränken & Adressbereiche, lokale und Remote-Ports & Portbereiche und das Sitzungsprotokoll, das aufgezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1b925-113">Filters can restrict packets on local and remote IP addresses & address ranges, local and remote ports & port ranges, and the session level protocol to be captured.</span></span> <span data-ttu-id="1b925-114">Filter sind kompostierbar, und es können mehrere Filter angewendet werden, um eine Granularität der Aufnahme zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="1b925-114">Filters are composable, and multiple filters can be applied to provide you with granularity of capture.</span></span>

## <span data-ttu-id="1b925-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1b925-115">EXAMPLES</span></span>

### <span data-ttu-id="1b925-116">Beispiel 1: Erstellen einer Paketerfassung mit mehreren Filtern</span><span class="sxs-lookup"><span data-stu-id="1b925-116">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filter $filter1, $filter2
```

<span data-ttu-id="1b925-117">In diesem Beispiel erstellen wir eine Paketerfassung mit dem Namen "PacketCaptureTest" mit mehreren Filtern und einem Zeitlimit.</span><span class="sxs-lookup"><span data-stu-id="1b925-117">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="1b925-118">Nachdem die Sitzung abgeschlossen ist, wird Sie im angegebenen Speicherkonto gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1b925-118">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="1b925-119">Hinweis: die Azure Network Watcher-Erweiterung muss auf dem virtuellen Zielcomputer installiert sein, um Paketerfassungen erstellen zu können.</span><span class="sxs-lookup"><span data-stu-id="1b925-119">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="1b925-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b925-120">PARAMETERS</span></span>

### <span data-ttu-id="1b925-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b925-121">-AsJob</span></span>
<span data-ttu-id="1b925-122">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1b925-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1b925-123">-BytesToCapturePerPacket</span><span class="sxs-lookup"><span data-stu-id="1b925-123">-BytesToCapturePerPacket</span></span>
<span data-ttu-id="1b925-124">Bytes, die pro Paket erfasst werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1b925-124">Bytes to capture per packet.</span></span>

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

### <span data-ttu-id="1b925-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b925-125">-DefaultProfile</span></span>
<span data-ttu-id="1b925-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1b925-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b925-127">-Filter</span><span class="sxs-lookup"><span data-stu-id="1b925-127">-Filter</span></span>
<span data-ttu-id="1b925-128">Filter für die Paket Aufnahmesitzung.</span><span class="sxs-lookup"><span data-stu-id="1b925-128">Filters for packet capture session.</span></span>

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

### <span data-ttu-id="1b925-129">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="1b925-129">-LocalFilePath</span></span>
<span data-ttu-id="1b925-130">Lokaler Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="1b925-130">Local file path.</span></span>

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

### <span data-ttu-id="1b925-131">-Standort</span><span class="sxs-lookup"><span data-stu-id="1b925-131">-Location</span></span>
<span data-ttu-id="1b925-132">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="1b925-132">Location of the network watcher.</span></span>

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

### <span data-ttu-id="1b925-133">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1b925-133">-NetworkWatcher</span></span>
<span data-ttu-id="1b925-134">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="1b925-134">The network watcher resource.</span></span>

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

### <span data-ttu-id="1b925-135">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="1b925-135">-NetworkWatcherName</span></span>
<span data-ttu-id="1b925-136">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="1b925-136">The name of network watcher.</span></span>

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

### <span data-ttu-id="1b925-137">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="1b925-137">-PacketCaptureName</span></span>
<span data-ttu-id="1b925-138">Der Name der Paketaufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="1b925-138">The packet capture name.</span></span>

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

### <span data-ttu-id="1b925-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b925-139">-ResourceGroupName</span></span>
<span data-ttu-id="1b925-140">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="1b925-140">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="1b925-141">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="1b925-141">-StorageAccountId</span></span>
<span data-ttu-id="1b925-142">Speicherkonto-ID.</span><span class="sxs-lookup"><span data-stu-id="1b925-142">Storage account Id.</span></span>

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

### <span data-ttu-id="1b925-143">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="1b925-143">-StoragePath</span></span>
<span data-ttu-id="1b925-144">Speicherpfad.</span><span class="sxs-lookup"><span data-stu-id="1b925-144">Storage path.</span></span>

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

### <span data-ttu-id="1b925-145">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="1b925-145">-TargetVirtualMachineId</span></span>
<span data-ttu-id="1b925-146">Die ID des virtuellen Zielcomputers</span><span class="sxs-lookup"><span data-stu-id="1b925-146">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="1b925-147">-TimeLimitInSeconds</span><span class="sxs-lookup"><span data-stu-id="1b925-147">-TimeLimitInSeconds</span></span>
<span data-ttu-id="1b925-148">Zeitlimit in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="1b925-148">Time limit in seconds.</span></span>

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

### <span data-ttu-id="1b925-149">-TotalBytesPerSession</span><span class="sxs-lookup"><span data-stu-id="1b925-149">-TotalBytesPerSession</span></span>
<span data-ttu-id="1b925-150">Gesamtanzahl der Bytes pro Sitzung.</span><span class="sxs-lookup"><span data-stu-id="1b925-150">Total bytes per session.</span></span>

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

### <span data-ttu-id="1b925-151">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1b925-151">-Confirm</span></span>
<span data-ttu-id="1b925-152">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1b925-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b925-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b925-153">-WhatIf</span></span>
<span data-ttu-id="1b925-154">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1b925-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b925-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1b925-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b925-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b925-156">CommonParameters</span></span>
<span data-ttu-id="1b925-157">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b925-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b925-158">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b925-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b925-159">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1b925-159">INPUTS</span></span>

### <span data-ttu-id="1b925-160">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1b925-160">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="1b925-161">System. String</span><span class="sxs-lookup"><span data-stu-id="1b925-161">System.String</span></span>

### <span data-ttu-id="1b925-162">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1b925-162">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="1b925-163">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1b925-163">OUTPUTS</span></span>

### <span data-ttu-id="1b925-164">Microsoft. Azure. Commands. Network. Models. PSPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="1b925-164">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureResult</span></span>

## <span data-ttu-id="1b925-165">Notizen</span><span class="sxs-lookup"><span data-stu-id="1b925-165">NOTES</span></span>
<span data-ttu-id="1b925-166">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerk Watcher, Paket, Capture, Traffic</span><span class="sxs-lookup"><span data-stu-id="1b925-166">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span> 

## <span data-ttu-id="1b925-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1b925-167">RELATED LINKS</span></span>

[<span data-ttu-id="1b925-168">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1b925-168">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="1b925-169">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1b925-169">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="1b925-170">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1b925-170">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="1b925-171">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="1b925-171">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="1b925-172">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="1b925-172">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="1b925-173">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="1b925-173">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="1b925-174">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="1b925-174">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="1b925-175">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1b925-175">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1b925-176">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="1b925-176">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="1b925-177">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1b925-177">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1b925-178">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1b925-178">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1b925-179">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1b925-179">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1b925-180">Neu – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="1b925-180">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="1b925-181">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="1b925-181">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="1b925-182">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="1b925-182">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="1b925-183">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1b925-183">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1b925-184">Anfang-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1b925-184">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1b925-185">Satz-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1b925-185">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1b925-186">Satz-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="1b925-186">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="1b925-187">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1b925-187">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1b925-188">Neu – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1b925-188">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="1b925-189">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="1b925-189">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="1b925-190">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="1b925-190">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="1b925-191">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="1b925-191">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="1b925-192">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="1b925-192">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="1b925-193">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="1b925-193">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="1b925-194">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="1b925-194">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)


