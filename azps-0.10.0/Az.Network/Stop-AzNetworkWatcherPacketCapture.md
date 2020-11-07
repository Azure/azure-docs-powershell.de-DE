---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: c4d31de526132974defc6b3d28542e1ec8de4c67
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843515"
---
# <span data-ttu-id="19c58-101">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="19c58-101">Stop-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="19c58-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="19c58-102">SYNOPSIS</span></span>
<span data-ttu-id="19c58-103">Beendet eine laufende Paket Aufnahmesitzung</span><span class="sxs-lookup"><span data-stu-id="19c58-103">Stops a running packet capture session</span></span>

## <span data-ttu-id="19c58-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="19c58-104">SYNTAX</span></span>

### <span data-ttu-id="19c58-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="19c58-105">SetByResource (Default)</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19c58-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="19c58-106">SetByName</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19c58-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="19c58-107">DESCRIPTION</span></span>
<span data-ttu-id="19c58-108">Die Stop-AzNetworkWatcherPacketCapture beendet eine laufende Paket Aufnahmesitzung.</span><span class="sxs-lookup"><span data-stu-id="19c58-108">The Stop-AzNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="19c58-109">Nachdem die Sitzung beendet wurde, wird die Paket Erfassungs Datei je nach Konfiguration in den Speicher hochgeladen und/oder lokal auf dem virtuellen Computer gespeichert.</span><span class="sxs-lookup"><span data-stu-id="19c58-109">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="19c58-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="19c58-110">EXAMPLES</span></span>

### <span data-ttu-id="19c58-111">---Beispiel 1: Beenden einer Paket Aufnahmesitzung---</span><span class="sxs-lookup"><span data-stu-id="19c58-111">--- Example 1: Stop a packet capture session ---</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="19c58-112">In diesem Beispiel wird eine laufende Packet Capture-Sitzung mit dem Namen "PacketCaptureTest" beendet.</span><span class="sxs-lookup"><span data-stu-id="19c58-112">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="19c58-113">Nachdem die Sitzung beendet wurde, wird die Paket Erfassungs Datei je nach Konfiguration in den Speicher hochgeladen und/oder lokal auf dem virtuellen Computer gespeichert.</span><span class="sxs-lookup"><span data-stu-id="19c58-113">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="19c58-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="19c58-114">PARAMETERS</span></span>

### <span data-ttu-id="19c58-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="19c58-115">-AsJob</span></span>
<span data-ttu-id="19c58-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="19c58-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="19c58-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19c58-117">-DefaultProfile</span></span>
<span data-ttu-id="19c58-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="19c58-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19c58-119">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="19c58-119">-NetworkWatcher</span></span>
<span data-ttu-id="19c58-120">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="19c58-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="19c58-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="19c58-121">-NetworkWatcherName</span></span>
<span data-ttu-id="19c58-122">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="19c58-122">The name of network watcher.</span></span>

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

### <span data-ttu-id="19c58-123">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="19c58-123">-PacketCaptureName</span></span>
<span data-ttu-id="19c58-124">Der Name der Paketaufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="19c58-124">The packet capture name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19c58-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19c58-125">-PassThru</span></span>
<span data-ttu-id="19c58-126">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="19c58-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="19c58-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19c58-127">-ResourceGroupName</span></span>
<span data-ttu-id="19c58-128">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="19c58-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="19c58-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="19c58-129">-Confirm</span></span>
<span data-ttu-id="19c58-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="19c58-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19c58-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19c58-131">-WhatIf</span></span>
<span data-ttu-id="19c58-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="19c58-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19c58-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="19c58-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19c58-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19c58-134">CommonParameters</span></span>
<span data-ttu-id="19c58-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19c58-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19c58-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19c58-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19c58-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="19c58-137">INPUTS</span></span>

### <span data-ttu-id="19c58-138">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="19c58-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="19c58-139">System. String</span><span class="sxs-lookup"><span data-stu-id="19c58-139">System.String</span></span>

## <span data-ttu-id="19c58-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="19c58-140">OUTPUTS</span></span>

### <span data-ttu-id="19c58-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="19c58-141">System.Boolean</span></span>

## <span data-ttu-id="19c58-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="19c58-142">NOTES</span></span>
<span data-ttu-id="19c58-143">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerk Watcher, Paket, Capture, Traffic</span><span class="sxs-lookup"><span data-stu-id="19c58-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="19c58-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="19c58-144">RELATED LINKS</span></span>

[<span data-ttu-id="19c58-145">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="19c58-145">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="19c58-146">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="19c58-146">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="19c58-147">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="19c58-147">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="19c58-148">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="19c58-148">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="19c58-149">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="19c58-149">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="19c58-150">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="19c58-150">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="19c58-151">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="19c58-151">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="19c58-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="19c58-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="19c58-153">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="19c58-153">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="19c58-154">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="19c58-154">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="19c58-155">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="19c58-155">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="19c58-156">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="19c58-156">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
