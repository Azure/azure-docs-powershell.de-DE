---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 87ae0ab7be4ace85d9f02a5637ea29dd27b0ae14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501726"
---
# <span data-ttu-id="ac328-101">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ac328-101">New-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="ac328-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ac328-102">SYNOPSIS</span></span>
<span data-ttu-id="ac328-103">Erstellt eine neue Paket Erfassungs Ressource und startet eine Paket Aufnahmesitzung auf einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="ac328-103">Creates a new packet capture resource and starts a packet capture session on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac328-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac328-104">SYNTAX</span></span>

### <span data-ttu-id="ac328-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="ac328-105">SetByResource (Default)</span></span>
```
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac328-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="ac328-106">SetByName</span></span>
```
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> -TargetVirtualMachineId <String> [-StorageAccountId <String>]
 [-StoragePath <String>] [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>]
 [-TotalBytesPerSession <Int32>] [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac328-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ac328-107">DESCRIPTION</span></span>
<span data-ttu-id="ac328-108">Das New-AzureRmNetworkWatcherPacketCapture-Cmdlet erstellt eine neue Paket Erfassungs Ressource und startet eine Paket Aufnahmesitzung auf einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="ac328-108">The New-AzureRmNetworkWatcherPacketCapture cmdlet creates a new packet capture resource and starts a packet capture session on a VM.</span></span>
<span data-ttu-id="ac328-109">Die Länge der Paket Aufnahmesitzungen kann über eine Zeitbeschränkung oder eine Größenbeschränkung konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="ac328-109">The length of the Packet Capture sessions can be configured via a time constraint or a size constraint.</span></span> <span data-ttu-id="ac328-110">Die für die einzelnen Pakete erfassten Datenmengen können ebenfalls konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="ac328-110">The amount of data captured for each packet can also be configured.</span></span>
<span data-ttu-id="ac328-111">Filter können auf eine bestimmte Paket Aufnahmesitzung angewendet werden, sodass Sie den Typ der erfassten Pakete anpassen können.</span><span class="sxs-lookup"><span data-stu-id="ac328-111">Filters can be applied to a given packet capture session, allowing you to customize the type of packets captured.</span></span> <span data-ttu-id="ac328-112">Filter können Pakete für lokale und Remote-IP-Adressen einschränken & Adressbereiche, lokale und Remote-Ports & Portbereiche und das Sitzungsprotokoll, das aufgezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ac328-112">Filters can restrict packets on local and remote IP addresses & address ranges, local and remote ports & port ranges, and the session level protocol to be captured.</span></span> <span data-ttu-id="ac328-113">Filter sind kompostierbar, und es können mehrere Filter angewendet werden, um eine Granularität der Aufnahme zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="ac328-113">Filters are composable, and multiple filters can be applied to provide you with granularity of capture.</span></span>

## <span data-ttu-id="ac328-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ac328-114">EXAMPLES</span></span>

### <span data-ttu-id="ac328-115">---Beispiel 1: Erstellen einer Paketerfassung mit mehreren Filtern---</span><span class="sxs-lookup"><span data-stu-id="ac328-115">--- Example 1: Create a Packet Capture with multiple filters ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filter $filter1, $filter2
```

<span data-ttu-id="ac328-116">In diesem Beispiel erstellen wir eine Paketerfassung mit dem Namen "PacketCaptureTest" mit mehreren Filtern und einem Zeitlimit.</span><span class="sxs-lookup"><span data-stu-id="ac328-116">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="ac328-117">Nachdem die Sitzung abgeschlossen ist, wird Sie im angegebenen Speicherkonto gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ac328-117">Once the session is complete, it will be saved to the specified storage account.</span></span> 

<span data-ttu-id="ac328-118">Hinweis: die Azure Network Watcher-Erweiterung muss auf dem virtuellen Zielcomputer installiert sein, um Paketerfassungen erstellen zu können.</span><span class="sxs-lookup"><span data-stu-id="ac328-118">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="ac328-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac328-119">PARAMETERS</span></span>

### <span data-ttu-id="ac328-120">-BytesToCapturePerPacket</span><span class="sxs-lookup"><span data-stu-id="ac328-120">-BytesToCapturePerPacket</span></span>
<span data-ttu-id="ac328-121">Bytes, die pro Paket erfasst werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ac328-121">Bytes to capture per packet.</span></span>

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

### <span data-ttu-id="ac328-122">-Filter</span><span class="sxs-lookup"><span data-stu-id="ac328-122">-Filter</span></span>
<span data-ttu-id="ac328-123">Filter für die Paket Aufnahmesitzung.</span><span class="sxs-lookup"><span data-stu-id="ac328-123">Filters for packet capture session.</span></span>

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

### <span data-ttu-id="ac328-124">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="ac328-124">-LocalFilePath</span></span>
<span data-ttu-id="ac328-125">Lokaler Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="ac328-125">Local file path.</span></span>

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

### <span data-ttu-id="ac328-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ac328-126">-NetworkWatcher</span></span>
<span data-ttu-id="ac328-127">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="ac328-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="ac328-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="ac328-128">-NetworkWatcherName</span></span>
<span data-ttu-id="ac328-129">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="ac328-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="ac328-130">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="ac328-130">-PacketCaptureName</span></span>
<span data-ttu-id="ac328-131">Der Name der Paketaufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="ac328-131">The packet capture name.</span></span>

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

### <span data-ttu-id="ac328-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac328-132">-ResourceGroupName</span></span>
<span data-ttu-id="ac328-133">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="ac328-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="ac328-134">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="ac328-134">-StorageAccountId</span></span>
<span data-ttu-id="ac328-135">Speicherkonto-ID.</span><span class="sxs-lookup"><span data-stu-id="ac328-135">Storage account Id.</span></span>

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

### <span data-ttu-id="ac328-136">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="ac328-136">-StoragePath</span></span>
<span data-ttu-id="ac328-137">Speicherpfad.</span><span class="sxs-lookup"><span data-stu-id="ac328-137">Storage path.</span></span>

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

### <span data-ttu-id="ac328-138">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="ac328-138">-TargetVirtualMachineId</span></span>
<span data-ttu-id="ac328-139">Die ID des virtuellen Zielcomputers</span><span class="sxs-lookup"><span data-stu-id="ac328-139">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="ac328-140">-TimeLimitInSeconds</span><span class="sxs-lookup"><span data-stu-id="ac328-140">-TimeLimitInSeconds</span></span>
<span data-ttu-id="ac328-141">Zeitlimit in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="ac328-141">Time limit in seconds.</span></span>

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

### <span data-ttu-id="ac328-142">-TotalBytesPerSession</span><span class="sxs-lookup"><span data-stu-id="ac328-142">-TotalBytesPerSession</span></span>
<span data-ttu-id="ac328-143">Gesamtanzahl der Bytes pro Sitzung.</span><span class="sxs-lookup"><span data-stu-id="ac328-143">Total bytes per session.</span></span>

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

### <span data-ttu-id="ac328-144">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ac328-144">-Confirm</span></span>
<span data-ttu-id="ac328-145">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ac328-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac328-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac328-146">-WhatIf</span></span>
<span data-ttu-id="ac328-147">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ac328-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac328-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ac328-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac328-149">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac328-149">-DefaultProfile</span></span>
<span data-ttu-id="ac328-150">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ac328-150">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac328-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac328-151">CommonParameters</span></span>
<span data-ttu-id="ac328-152">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac328-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac328-153">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac328-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac328-154">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ac328-154">INPUTS</span></span>

### <span data-ttu-id="ac328-155">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ac328-155">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="ac328-156">System. String System. Nullable \` 1 \[ \[ System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089\]\]</span><span class="sxs-lookup"><span data-stu-id="ac328-156">System.String System.Nullable\`1\[\[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\]</span></span>

## <span data-ttu-id="ac328-157">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ac328-157">OUTPUTS</span></span>

### <span data-ttu-id="ac328-158">Microsoft. Azure. Commands. Network. Models. PSPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ac328-158">Microsoft.Azure.Commands.Network.Models.PSPacketCapture</span></span>

## <span data-ttu-id="ac328-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="ac328-159">NOTES</span></span>
<span data-ttu-id="ac328-160">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerk Watcher, Paket, Capture, Traffic</span><span class="sxs-lookup"><span data-stu-id="ac328-160">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span> 

## <span data-ttu-id="ac328-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ac328-161">RELATED LINKS</span></span>

[<span data-ttu-id="ac328-162">Neu – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ac328-162">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="ac328-163">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ac328-163">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ac328-164">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ac328-164">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ac328-165">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ac328-165">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ac328-166">Neu – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ac328-166">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="ac328-167">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ac328-167">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="ac328-168">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ac328-168">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="ac328-169">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="ac328-169">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="ac328-170">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="ac328-170">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="ac328-171">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="ac328-171">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="ac328-172">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="ac328-172">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="ac328-173">Anfang-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="ac328-173">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)


