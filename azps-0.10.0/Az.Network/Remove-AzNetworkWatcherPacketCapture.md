---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: b3095aace7fa8e1959e51ef64aa92b6d2bcaffba
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843792"
---
# <span data-ttu-id="964d8-101">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="964d8-101">Remove-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="964d8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="964d8-102">SYNOPSIS</span></span>
<span data-ttu-id="964d8-103">Entfernt eine Paket Erfassungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="964d8-103">Removes a packet capture resource.</span></span>

## <span data-ttu-id="964d8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="964d8-104">SYNTAX</span></span>

### <span data-ttu-id="964d8-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="964d8-105">SetByResource (Default)</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="964d8-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="964d8-106">SetByName</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="964d8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="964d8-107">DESCRIPTION</span></span>
<span data-ttu-id="964d8-108">Die Remove-AzNetworkWatcherPacketCapture entfernt eine Sammlungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="964d8-108">The Remove-AzNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="964d8-109">Es wird empfohlen, Stop-AzNetworkWatcherPacketCapture aufzurufen, bevor Sie Remove-AzNetworkWatcherPacketCapture aufrufen.</span><span class="sxs-lookup"><span data-stu-id="964d8-109">It is recommended to call Stop-AzNetworkWatcherPacketCapture before calling Remove-AzNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="964d8-110">Wenn die Paket Aufnahmesitzung ausgeführt wird, wenn Remove-AzNetworkWatcherPacketCapture aufgerufen wird, wird die Paketerfassung möglicherweise nicht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="964d8-110">If the packet capture session is running when Remove-AzNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="964d8-111">Wenn die Sitzung vor dem Entfernen angehalten wird, wird die Cap-Datei, die die Aufnahmedaten enthält, nicht entfernt.</span><span class="sxs-lookup"><span data-stu-id="964d8-111">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="964d8-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="964d8-112">EXAMPLES</span></span>

### <span data-ttu-id="964d8-113">---Beispiel 1: Entfernen einer Paket Aufnahmesitzung--</span><span class="sxs-lookup"><span data-stu-id="964d8-113">--- Example 1: Remove a packet capture session --</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="964d8-114">In diesem Beispiel wird eine vorhandene Paket erfassungssitzung mit dem Namen "PacketCaptureTest" entfernt.</span><span class="sxs-lookup"><span data-stu-id="964d8-114">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="964d8-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="964d8-115">PARAMETERS</span></span>

### <span data-ttu-id="964d8-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="964d8-116">-AsJob</span></span>
<span data-ttu-id="964d8-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="964d8-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="964d8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="964d8-118">-DefaultProfile</span></span>
<span data-ttu-id="964d8-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="964d8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="964d8-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="964d8-120">-NetworkWatcher</span></span>
<span data-ttu-id="964d8-121">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="964d8-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="964d8-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="964d8-122">-NetworkWatcherName</span></span>
<span data-ttu-id="964d8-123">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="964d8-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="964d8-124">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="964d8-124">-PacketCaptureName</span></span>
<span data-ttu-id="964d8-125">Der Name der Paketaufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="964d8-125">The packet capture name.</span></span>

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

### <span data-ttu-id="964d8-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="964d8-126">-PassThru</span></span>
<span data-ttu-id="964d8-127">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="964d8-127">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="964d8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="964d8-128">-ResourceGroupName</span></span>
<span data-ttu-id="964d8-129">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="964d8-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="964d8-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="964d8-130">-Confirm</span></span>
<span data-ttu-id="964d8-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="964d8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="964d8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="964d8-132">-WhatIf</span></span>
<span data-ttu-id="964d8-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="964d8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="964d8-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="964d8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="964d8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="964d8-135">CommonParameters</span></span>
<span data-ttu-id="964d8-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="964d8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="964d8-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="964d8-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="964d8-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="964d8-138">INPUTS</span></span>

### <span data-ttu-id="964d8-139">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="964d8-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="964d8-140">System. String</span><span class="sxs-lookup"><span data-stu-id="964d8-140">System.String</span></span>

## <span data-ttu-id="964d8-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="964d8-141">OUTPUTS</span></span>

### <span data-ttu-id="964d8-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="964d8-142">System.Object</span></span>

## <span data-ttu-id="964d8-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="964d8-143">NOTES</span></span>
<span data-ttu-id="964d8-144">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerkmonitor, Paket, erfassen, Datenverkehr, entfernen</span><span class="sxs-lookup"><span data-stu-id="964d8-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="964d8-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="964d8-145">RELATED LINKS</span></span>

[<span data-ttu-id="964d8-146">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="964d8-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="964d8-147">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="964d8-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="964d8-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="964d8-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="964d8-149">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="964d8-149">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="964d8-150">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="964d8-150">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="964d8-151">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="964d8-151">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="964d8-152">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="964d8-152">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="964d8-153">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="964d8-153">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="964d8-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="964d8-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="964d8-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="964d8-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="964d8-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="964d8-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="964d8-157">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="964d8-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
