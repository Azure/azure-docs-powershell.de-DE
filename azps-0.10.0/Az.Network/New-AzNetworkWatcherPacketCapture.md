---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 6844db506ee8a55c7d0c16f54946e35349059ae4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841284"
---
# <span data-ttu-id="b48ab-101">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b48ab-101">New-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="b48ab-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b48ab-102">SYNOPSIS</span></span>
<span data-ttu-id="b48ab-103">Erstellt eine neue Paket Erfassungs Ressource und startet eine Paket Aufnahmesitzung auf einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="b48ab-103">Creates a new packet capture resource and starts a packet capture session on a VM.</span></span>

## <span data-ttu-id="b48ab-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b48ab-104">SYNTAX</span></span>

### <span data-ttu-id="b48ab-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="b48ab-105">SetByResource (Default)</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b48ab-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="b48ab-106">SetByName</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> -TargetVirtualMachineId <String> [-StorageAccountId <String>]
 [-StoragePath <String>] [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>]
 [-TotalBytesPerSession <Int32>] [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b48ab-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b48ab-107">DESCRIPTION</span></span>
<span data-ttu-id="b48ab-108">Das New-AzNetworkWatcherPacketCapture-Cmdlet erstellt eine neue Paket Erfassungs Ressource und startet eine Paket Aufnahmesitzung auf einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="b48ab-108">The New-AzNetworkWatcherPacketCapture cmdlet creates a new packet capture resource and starts a packet capture session on a VM.</span></span>
<span data-ttu-id="b48ab-109">Die Länge der Paket Aufnahmesitzungen kann über eine Zeitbeschränkung oder eine Größenbeschränkung konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="b48ab-109">The length of the Packet Capture sessions can be configured via a time constraint or a size constraint.</span></span> <span data-ttu-id="b48ab-110">Die für die einzelnen Pakete erfassten Datenmengen können ebenfalls konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="b48ab-110">The amount of data captured for each packet can also be configured.</span></span>
<span data-ttu-id="b48ab-111">Filter können auf eine bestimmte Paket Aufnahmesitzung angewendet werden, sodass Sie den Typ der erfassten Pakete anpassen können.</span><span class="sxs-lookup"><span data-stu-id="b48ab-111">Filters can be applied to a given packet capture session, allowing you to customize the type of packets captured.</span></span> <span data-ttu-id="b48ab-112">Filter können Pakete für lokale und Remote-IP-Adressen einschränken & Adressbereiche, lokale und Remote-Ports & Portbereiche und das Sitzungsprotokoll, das aufgezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b48ab-112">Filters can restrict packets on local and remote IP addresses & address ranges, local and remote ports & port ranges, and the session level protocol to be captured.</span></span> <span data-ttu-id="b48ab-113">Filter sind kompostierbar, und es können mehrere Filter angewendet werden, um eine Granularität der Aufnahme zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="b48ab-113">Filters are composable, and multiple filters can be applied to provide you with granularity of capture.</span></span>

## <span data-ttu-id="b48ab-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b48ab-114">EXAMPLES</span></span>

### <span data-ttu-id="b48ab-115">---Beispiel 1: Erstellen einer Paketerfassung mit mehreren Filtern---</span><span class="sxs-lookup"><span data-stu-id="b48ab-115">--- Example 1: Create a Packet Capture with multiple filters ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filter $filter1, $filter2
```

<span data-ttu-id="b48ab-116">In diesem Beispiel erstellen wir eine Paketerfassung mit dem Namen "PacketCaptureTest" mit mehreren Filtern und einem Zeitlimit.</span><span class="sxs-lookup"><span data-stu-id="b48ab-116">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="b48ab-117">Nachdem die Sitzung abgeschlossen ist, wird Sie im angegebenen Speicherkonto gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b48ab-117">Once the session is complete, it will be saved to the specified storage account.</span></span> 

<span data-ttu-id="b48ab-118">Hinweis: die Azure Network Watcher-Erweiterung muss auf dem virtuellen Zielcomputer installiert sein, um Paketerfassungen erstellen zu können.</span><span class="sxs-lookup"><span data-stu-id="b48ab-118">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="b48ab-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="b48ab-119">PARAMETERS</span></span>

### <span data-ttu-id="b48ab-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b48ab-120">-AsJob</span></span>
<span data-ttu-id="b48ab-121">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b48ab-121">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b48ab-122">-BytesToCapturePerPacket</span><span class="sxs-lookup"><span data-stu-id="b48ab-122">-BytesToCapturePerPacket</span></span>
<span data-ttu-id="b48ab-123">Bytes, die pro Paket erfasst werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b48ab-123">Bytes to capture per packet.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b48ab-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b48ab-124">-DefaultProfile</span></span>
<span data-ttu-id="b48ab-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b48ab-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b48ab-126">-Filter</span><span class="sxs-lookup"><span data-stu-id="b48ab-126">-Filter</span></span>
<span data-ttu-id="b48ab-127">Filter für die Paket Aufnahmesitzung.</span><span class="sxs-lookup"><span data-stu-id="b48ab-127">Filters for packet capture session.</span></span>

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

### <span data-ttu-id="b48ab-128">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="b48ab-128">-LocalFilePath</span></span>
<span data-ttu-id="b48ab-129">Lokaler Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="b48ab-129">Local file path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b48ab-130">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b48ab-130">-NetworkWatcher</span></span>
<span data-ttu-id="b48ab-131">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="b48ab-131">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b48ab-132">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="b48ab-132">-NetworkWatcherName</span></span>
<span data-ttu-id="b48ab-133">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="b48ab-133">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b48ab-134">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="b48ab-134">-PacketCaptureName</span></span>
<span data-ttu-id="b48ab-135">Der Name der Paketaufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="b48ab-135">The packet capture name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b48ab-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b48ab-136">-ResourceGroupName</span></span>
<span data-ttu-id="b48ab-137">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="b48ab-137">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b48ab-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="b48ab-138">-StorageAccountId</span></span>
<span data-ttu-id="b48ab-139">Speicherkonto-ID.</span><span class="sxs-lookup"><span data-stu-id="b48ab-139">Storage account Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b48ab-140">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="b48ab-140">-StoragePath</span></span>
<span data-ttu-id="b48ab-141">Speicherpfad.</span><span class="sxs-lookup"><span data-stu-id="b48ab-141">Storage path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b48ab-142">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="b48ab-142">-TargetVirtualMachineId</span></span>
<span data-ttu-id="b48ab-143">Die ID des virtuellen Zielcomputers</span><span class="sxs-lookup"><span data-stu-id="b48ab-143">The target virtual machine ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b48ab-144">-TimeLimitInSeconds</span><span class="sxs-lookup"><span data-stu-id="b48ab-144">-TimeLimitInSeconds</span></span>
<span data-ttu-id="b48ab-145">Zeitlimit in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="b48ab-145">Time limit in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b48ab-146">-TotalBytesPerSession</span><span class="sxs-lookup"><span data-stu-id="b48ab-146">-TotalBytesPerSession</span></span>
<span data-ttu-id="b48ab-147">Gesamtanzahl der Bytes pro Sitzung.</span><span class="sxs-lookup"><span data-stu-id="b48ab-147">Total bytes per session.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b48ab-148">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b48ab-148">-Confirm</span></span>
<span data-ttu-id="b48ab-149">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b48ab-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b48ab-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b48ab-150">-WhatIf</span></span>
<span data-ttu-id="b48ab-151">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b48ab-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b48ab-152">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b48ab-152">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b48ab-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b48ab-153">CommonParameters</span></span>
<span data-ttu-id="b48ab-154">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b48ab-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b48ab-155">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b48ab-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b48ab-156">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b48ab-156">INPUTS</span></span>

### <span data-ttu-id="b48ab-157">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b48ab-157">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="b48ab-158">System. String System. Nullable \` 1 \[ \[ System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089\]\]</span><span class="sxs-lookup"><span data-stu-id="b48ab-158">System.String System.Nullable\`1\[\[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\]</span></span>

## <span data-ttu-id="b48ab-159">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b48ab-159">OUTPUTS</span></span>

### <span data-ttu-id="b48ab-160">Microsoft. Azure. Commands. Network. Models. PSPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b48ab-160">Microsoft.Azure.Commands.Network.Models.PSPacketCapture</span></span>

## <span data-ttu-id="b48ab-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="b48ab-161">NOTES</span></span>
<span data-ttu-id="b48ab-162">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerk Watcher, Paket, Capture, Traffic</span><span class="sxs-lookup"><span data-stu-id="b48ab-162">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span> 

## <span data-ttu-id="b48ab-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b48ab-163">RELATED LINKS</span></span>

[<span data-ttu-id="b48ab-164">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="b48ab-164">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="b48ab-165">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b48ab-165">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b48ab-166">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b48ab-166">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b48ab-167">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b48ab-167">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b48ab-168">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b48ab-168">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="b48ab-169">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b48ab-169">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="b48ab-170">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b48ab-170">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="b48ab-171">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="b48ab-171">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="b48ab-172">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="b48ab-172">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="b48ab-173">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="b48ab-173">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="b48ab-174">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="b48ab-174">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="b48ab-175">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="b48ab-175">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)


