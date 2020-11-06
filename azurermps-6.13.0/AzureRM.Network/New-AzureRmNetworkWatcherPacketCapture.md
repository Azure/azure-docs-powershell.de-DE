---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: ab7b6176f8453d1a3e5e0001e6b6c1e47c4de1cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505329"
---
# <span data-ttu-id="d3034-101">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d3034-101">New-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="d3034-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d3034-102">SYNOPSIS</span></span>
<span data-ttu-id="d3034-103">Erstellt eine neue Paket Erfassungs Ressource und startet eine Paket Aufnahmesitzung auf einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="d3034-103">Creates a new packet capture resource and starts a packet capture session on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3034-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3034-104">SYNTAX</span></span>

### <span data-ttu-id="d3034-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="d3034-105">SetByResource (Default)</span></span>
```
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3034-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="d3034-106">SetByName</span></span>
```
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> -TargetVirtualMachineId <String> [-StorageAccountId <String>]
 [-StoragePath <String>] [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>]
 [-TotalBytesPerSession <Int32>] [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3034-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="d3034-107">SetByLocation</span></span>
```
New-AzureRmNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3034-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d3034-108">DESCRIPTION</span></span>
<span data-ttu-id="d3034-109">Das New-AzureRmNetworkWatcherPacketCapture-Cmdlet erstellt eine neue Paket Erfassungs Ressource und startet eine Paket Aufnahmesitzung auf einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="d3034-109">The New-AzureRmNetworkWatcherPacketCapture cmdlet creates a new packet capture resource and starts a packet capture session on a VM.</span></span>
<span data-ttu-id="d3034-110">Die Länge der Paket Aufnahmesitzungen kann über eine Zeitbeschränkung oder eine Größenbeschränkung konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="d3034-110">The length of the Packet Capture sessions can be configured via a time constraint or a size constraint.</span></span> <span data-ttu-id="d3034-111">Die für die einzelnen Pakete erfassten Datenmengen können ebenfalls konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="d3034-111">The amount of data captured for each packet can also be configured.</span></span>
<span data-ttu-id="d3034-112">Filter können auf eine bestimmte Paket Aufnahmesitzung angewendet werden, sodass Sie den Typ der erfassten Pakete anpassen können.</span><span class="sxs-lookup"><span data-stu-id="d3034-112">Filters can be applied to a given packet capture session, allowing you to customize the type of packets captured.</span></span> <span data-ttu-id="d3034-113">Filter können Pakete für lokale und Remote-IP-Adressen einschränken & Adressbereiche, lokale und Remote-Ports & Portbereiche und das Sitzungsprotokoll, das aufgezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d3034-113">Filters can restrict packets on local and remote IP addresses & address ranges, local and remote ports & port ranges, and the session level protocol to be captured.</span></span> <span data-ttu-id="d3034-114">Filter sind kompostierbar, und es können mehrere Filter angewendet werden, um eine Granularität der Aufnahme zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="d3034-114">Filters are composable, and multiple filters can be applied to provide you with granularity of capture.</span></span>

## <span data-ttu-id="d3034-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d3034-115">EXAMPLES</span></span>

### <span data-ttu-id="d3034-116">Beispiel 1: Erstellen einer Paketerfassung mit mehreren Filtern</span><span class="sxs-lookup"><span data-stu-id="d3034-116">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filter $filter1, $filter2
```

<span data-ttu-id="d3034-117">In diesem Beispiel erstellen wir eine Paketerfassung mit dem Namen "PacketCaptureTest" mit mehreren Filtern und einem Zeitlimit.</span><span class="sxs-lookup"><span data-stu-id="d3034-117">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="d3034-118">Nachdem die Sitzung abgeschlossen ist, wird Sie im angegebenen Speicherkonto gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d3034-118">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="d3034-119">Hinweis: die Azure Network Watcher-Erweiterung muss auf dem virtuellen Zielcomputer installiert sein, um Paketerfassungen erstellen zu können.</span><span class="sxs-lookup"><span data-stu-id="d3034-119">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="d3034-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3034-120">PARAMETERS</span></span>

### <span data-ttu-id="d3034-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3034-121">-AsJob</span></span>
<span data-ttu-id="d3034-122">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d3034-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d3034-123">-BytesToCapturePerPacket</span><span class="sxs-lookup"><span data-stu-id="d3034-123">-BytesToCapturePerPacket</span></span>
<span data-ttu-id="d3034-124">Bytes, die pro Paket erfasst werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d3034-124">Bytes to capture per packet.</span></span>

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

### <span data-ttu-id="d3034-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3034-125">-DefaultProfile</span></span>
<span data-ttu-id="d3034-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d3034-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3034-127">-Filter</span><span class="sxs-lookup"><span data-stu-id="d3034-127">-Filter</span></span>
<span data-ttu-id="d3034-128">Filter für die Paket Aufnahmesitzung.</span><span class="sxs-lookup"><span data-stu-id="d3034-128">Filters for packet capture session.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3034-129">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="d3034-129">-LocalFilePath</span></span>
<span data-ttu-id="d3034-130">Lokaler Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="d3034-130">Local file path.</span></span>

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

### <span data-ttu-id="d3034-131">-Standort</span><span class="sxs-lookup"><span data-stu-id="d3034-131">-Location</span></span>
<span data-ttu-id="d3034-132">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="d3034-132">Location of the network watcher.</span></span>

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

### <span data-ttu-id="d3034-133">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d3034-133">-NetworkWatcher</span></span>
<span data-ttu-id="d3034-134">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="d3034-134">The network watcher resource.</span></span>

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

### <span data-ttu-id="d3034-135">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d3034-135">-NetworkWatcherName</span></span>
<span data-ttu-id="d3034-136">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="d3034-136">The name of network watcher.</span></span>

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

### <span data-ttu-id="d3034-137">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="d3034-137">-PacketCaptureName</span></span>
<span data-ttu-id="d3034-138">Der Name der Paketaufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="d3034-138">The packet capture name.</span></span>

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

### <span data-ttu-id="d3034-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3034-139">-ResourceGroupName</span></span>
<span data-ttu-id="d3034-140">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="d3034-140">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d3034-141">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="d3034-141">-StorageAccountId</span></span>
<span data-ttu-id="d3034-142">Speicherkonto-ID.</span><span class="sxs-lookup"><span data-stu-id="d3034-142">Storage account Id.</span></span>

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

### <span data-ttu-id="d3034-143">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="d3034-143">-StoragePath</span></span>
<span data-ttu-id="d3034-144">Speicherpfad.</span><span class="sxs-lookup"><span data-stu-id="d3034-144">Storage path.</span></span>

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

### <span data-ttu-id="d3034-145">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="d3034-145">-TargetVirtualMachineId</span></span>
<span data-ttu-id="d3034-146">Die ID des virtuellen Zielcomputers</span><span class="sxs-lookup"><span data-stu-id="d3034-146">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="d3034-147">-TimeLimitInSeconds</span><span class="sxs-lookup"><span data-stu-id="d3034-147">-TimeLimitInSeconds</span></span>
<span data-ttu-id="d3034-148">Zeitlimit in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="d3034-148">Time limit in seconds.</span></span>

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

### <span data-ttu-id="d3034-149">-TotalBytesPerSession</span><span class="sxs-lookup"><span data-stu-id="d3034-149">-TotalBytesPerSession</span></span>
<span data-ttu-id="d3034-150">Gesamtanzahl der Bytes pro Sitzung.</span><span class="sxs-lookup"><span data-stu-id="d3034-150">Total bytes per session.</span></span>

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

### <span data-ttu-id="d3034-151">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d3034-151">-Confirm</span></span>
<span data-ttu-id="d3034-152">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d3034-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3034-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3034-153">-WhatIf</span></span>
<span data-ttu-id="d3034-154">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d3034-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3034-155">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d3034-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3034-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3034-156">CommonParameters</span></span>
<span data-ttu-id="d3034-157">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3034-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3034-158">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3034-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3034-159">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d3034-159">INPUTS</span></span>

### <span data-ttu-id="d3034-160">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d3034-160">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="d3034-161">Parameter: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d3034-161">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="d3034-162">System. String</span><span class="sxs-lookup"><span data-stu-id="d3034-162">System.String</span></span>
<span data-ttu-id="d3034-163">Parameter: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d3034-163">Parameters: NetworkWatcherName (ByValue)</span></span>

### <span data-ttu-id="d3034-164">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d3034-164">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="d3034-165">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d3034-165">OUTPUTS</span></span>

### <span data-ttu-id="d3034-166">Microsoft. Azure. Commands. Network. Models. PSPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="d3034-166">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureResult</span></span>

## <span data-ttu-id="d3034-167">Notizen</span><span class="sxs-lookup"><span data-stu-id="d3034-167">NOTES</span></span>
<span data-ttu-id="d3034-168">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerk Watcher, Paket, Capture, Traffic</span><span class="sxs-lookup"><span data-stu-id="d3034-168">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span> 

## <span data-ttu-id="d3034-169">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d3034-169">RELATED LINKS</span></span>

[<span data-ttu-id="d3034-170">Neu – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d3034-170">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="d3034-171">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d3034-171">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="d3034-172">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d3034-172">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="d3034-173">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d3034-173">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="d3034-174">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d3034-174">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d3034-175">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d3034-175">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="d3034-176">Anfang-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d3034-176">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="d3034-177">Neu – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d3034-177">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d3034-178">Neu – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d3034-178">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="d3034-179">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d3034-179">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d3034-180">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d3034-180">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d3034-181">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d3034-181">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d3034-182">Neu – AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3034-182">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="d3034-183">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d3034-183">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="d3034-184">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="d3034-184">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="d3034-185">Stopp-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d3034-185">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d3034-186">Anfang-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d3034-186">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d3034-187">Satz-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d3034-187">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d3034-188">Satz-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="d3034-188">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="d3034-189">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d3034-189">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d3034-190">Neu – AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d3034-190">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d3034-191">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="d3034-191">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="d3034-192">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="d3034-192">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="d3034-193">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="d3034-193">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="d3034-194">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="d3034-194">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="d3034-195">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="d3034-195">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="d3034-196">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d3034-196">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)


