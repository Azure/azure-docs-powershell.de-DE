---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermnetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 43dc48aaa58f086e6d05f45a81096612d3177a17
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664623"
---
# <span data-ttu-id="85dc4-101">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="85dc4-101">Stop-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="85dc4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="85dc4-102">SYNOPSIS</span></span>
<span data-ttu-id="85dc4-103">Beendet eine laufende Paket Aufnahmesitzung</span><span class="sxs-lookup"><span data-stu-id="85dc4-103">Stops a running packet capture session</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85dc4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="85dc4-104">SYNTAX</span></span>

### <span data-ttu-id="85dc4-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="85dc4-105">SetByResource (Default)</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85dc4-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="85dc4-106">SetByName</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85dc4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="85dc4-107">DESCRIPTION</span></span>
<span data-ttu-id="85dc4-108">Die Stop-AzureRmNetworkWatcherPacketCapture beendet eine laufende Paket Aufnahmesitzung.</span><span class="sxs-lookup"><span data-stu-id="85dc4-108">The Stop-AzureRmNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="85dc4-109">Nachdem die Sitzung beendet wurde, wird die Paket Erfassungs Datei je nach Konfiguration in den Speicher hochgeladen und/oder lokal auf dem virtuellen Computer gespeichert.</span><span class="sxs-lookup"><span data-stu-id="85dc4-109">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="85dc4-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="85dc4-110">EXAMPLES</span></span>

### <span data-ttu-id="85dc4-111">---Beispiel 1: Beenden einer Paket Aufnahmesitzung---</span><span class="sxs-lookup"><span data-stu-id="85dc4-111">--- Example 1: Stop a packet capture session ---</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="85dc4-112">In diesem Beispiel wird eine laufende Packet Capture-Sitzung mit dem Namen "PacketCaptureTest" beendet.</span><span class="sxs-lookup"><span data-stu-id="85dc4-112">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="85dc4-113">Nachdem die Sitzung beendet wurde, wird die Paket Erfassungs Datei je nach Konfiguration in den Speicher hochgeladen und/oder lokal auf dem virtuellen Computer gespeichert.</span><span class="sxs-lookup"><span data-stu-id="85dc4-113">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="85dc4-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="85dc4-114">PARAMETERS</span></span>

### <span data-ttu-id="85dc4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="85dc4-115">-AsJob</span></span>
<span data-ttu-id="85dc4-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="85dc4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="85dc4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85dc4-117">-DefaultProfile</span></span>
<span data-ttu-id="85dc4-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="85dc4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85dc4-119">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="85dc4-119">-NetworkWatcher</span></span>
<span data-ttu-id="85dc4-120">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="85dc4-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="85dc4-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="85dc4-121">-NetworkWatcherName</span></span>
<span data-ttu-id="85dc4-122">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="85dc4-122">The name of network watcher.</span></span>

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

### <span data-ttu-id="85dc4-123">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="85dc4-123">-PacketCaptureName</span></span>
<span data-ttu-id="85dc4-124">Der Name der Paketaufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="85dc4-124">The packet capture name.</span></span>

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

### <span data-ttu-id="85dc4-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85dc4-125">-PassThru</span></span>
<span data-ttu-id="85dc4-126">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="85dc4-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="85dc4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85dc4-127">-ResourceGroupName</span></span>
<span data-ttu-id="85dc4-128">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="85dc4-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="85dc4-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="85dc4-129">-Confirm</span></span>
<span data-ttu-id="85dc4-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="85dc4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85dc4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85dc4-131">-WhatIf</span></span>
<span data-ttu-id="85dc4-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="85dc4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85dc4-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="85dc4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85dc4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85dc4-134">CommonParameters</span></span>
<span data-ttu-id="85dc4-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85dc4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85dc4-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85dc4-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85dc4-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="85dc4-137">INPUTS</span></span>

### <span data-ttu-id="85dc4-138">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="85dc4-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="85dc4-139">System. String</span><span class="sxs-lookup"><span data-stu-id="85dc4-139">System.String</span></span>

## <span data-ttu-id="85dc4-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="85dc4-140">OUTPUTS</span></span>

### <span data-ttu-id="85dc4-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="85dc4-141">System.Boolean</span></span>

## <span data-ttu-id="85dc4-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="85dc4-142">NOTES</span></span>
<span data-ttu-id="85dc4-143">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerk Watcher, Paket, Capture, Traffic</span><span class="sxs-lookup"><span data-stu-id="85dc4-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="85dc4-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="85dc4-144">RELATED LINKS</span></span>

[<span data-ttu-id="85dc4-145">Neu – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="85dc4-145">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="85dc4-146">Neu – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="85dc4-146">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="85dc4-147">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="85dc4-147">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="85dc4-148">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="85dc4-148">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="85dc4-149">Neu – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="85dc4-149">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="85dc4-150">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="85dc4-150">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="85dc4-151">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="85dc4-151">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="85dc4-152">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="85dc4-152">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="85dc4-153">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="85dc4-153">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="85dc4-154">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="85dc4-154">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="85dc4-155">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="85dc4-155">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="85dc4-156">Anfang-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="85dc4-156">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
