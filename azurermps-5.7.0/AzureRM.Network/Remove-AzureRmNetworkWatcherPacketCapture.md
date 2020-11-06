---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 034cca094bf6dd7d3911e3e705e03888f0ea10ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503065"
---
# <span data-ttu-id="865aa-101">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="865aa-101">Remove-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="865aa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="865aa-102">SYNOPSIS</span></span>
<span data-ttu-id="865aa-103">Entfernt eine Paket Erfassungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="865aa-103">Removes a packet capture resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="865aa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="865aa-104">SYNTAX</span></span>

### <span data-ttu-id="865aa-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="865aa-105">SetByResource (Default)</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="865aa-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="865aa-106">SetByName</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="865aa-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="865aa-107">DESCRIPTION</span></span>
<span data-ttu-id="865aa-108">Die Remove-AzureRmNetworkWatcherPacketCapture entfernt eine Sammlungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="865aa-108">The Remove-AzureRmNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="865aa-109">Es wird empfohlen, Stop-AzureRmNetworkWatcherPacketCapture aufzurufen, bevor Sie Remove-AzureRmNetworkWatcherPacketCapture aufrufen.</span><span class="sxs-lookup"><span data-stu-id="865aa-109">It is recommended to call Stop-AzureRmNetworkWatcherPacketCapture before calling Remove-AzureRmNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="865aa-110">Wenn die Paket Aufnahmesitzung ausgeführt wird, wenn Remove-AzureRmNetworkWatcherPacketCapture aufgerufen wird, wird die Paketerfassung möglicherweise nicht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="865aa-110">If the packet capture session is running when Remove-AzureRmNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="865aa-111">Wenn die Sitzung vor dem Entfernen angehalten wird, wird die Cap-Datei, die die Aufnahmedaten enthält, nicht entfernt.</span><span class="sxs-lookup"><span data-stu-id="865aa-111">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="865aa-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="865aa-112">EXAMPLES</span></span>

### <span data-ttu-id="865aa-113">---Beispiel 1: Entfernen einer Paket Aufnahmesitzung--</span><span class="sxs-lookup"><span data-stu-id="865aa-113">--- Example 1: Remove a packet capture session --</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="865aa-114">In diesem Beispiel wird eine vorhandene Paket erfassungssitzung mit dem Namen "PacketCaptureTest" entfernt.</span><span class="sxs-lookup"><span data-stu-id="865aa-114">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="865aa-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="865aa-115">PARAMETERS</span></span>

### <span data-ttu-id="865aa-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="865aa-116">-AsJob</span></span>
<span data-ttu-id="865aa-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="865aa-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="865aa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="865aa-118">-DefaultProfile</span></span>
<span data-ttu-id="865aa-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="865aa-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="865aa-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="865aa-120">-NetworkWatcher</span></span>
<span data-ttu-id="865aa-121">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="865aa-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="865aa-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="865aa-122">-NetworkWatcherName</span></span>
<span data-ttu-id="865aa-123">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="865aa-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="865aa-124">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="865aa-124">-PacketCaptureName</span></span>
<span data-ttu-id="865aa-125">Der Name der Paketaufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="865aa-125">The packet capture name.</span></span>

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

### <span data-ttu-id="865aa-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="865aa-126">-PassThru</span></span>
<span data-ttu-id="865aa-127">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="865aa-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="865aa-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="865aa-128">-ResourceGroupName</span></span>
<span data-ttu-id="865aa-129">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="865aa-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="865aa-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="865aa-130">-Confirm</span></span>
<span data-ttu-id="865aa-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="865aa-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="865aa-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="865aa-132">-WhatIf</span></span>
<span data-ttu-id="865aa-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="865aa-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="865aa-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="865aa-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="865aa-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="865aa-135">CommonParameters</span></span>
<span data-ttu-id="865aa-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="865aa-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="865aa-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="865aa-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="865aa-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="865aa-138">INPUTS</span></span>

### <span data-ttu-id="865aa-139">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="865aa-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="865aa-140">System. String</span><span class="sxs-lookup"><span data-stu-id="865aa-140">System.String</span></span>

## <span data-ttu-id="865aa-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="865aa-141">OUTPUTS</span></span>

### <span data-ttu-id="865aa-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="865aa-142">System.Object</span></span>

## <span data-ttu-id="865aa-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="865aa-143">NOTES</span></span>
<span data-ttu-id="865aa-144">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerkmonitor, Paket, erfassen, Datenverkehr, entfernen</span><span class="sxs-lookup"><span data-stu-id="865aa-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="865aa-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="865aa-145">RELATED LINKS</span></span>

[<span data-ttu-id="865aa-146">Neu – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="865aa-146">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="865aa-147">Neu – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="865aa-147">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="865aa-148">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="865aa-148">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="865aa-149">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="865aa-149">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="865aa-150">Neu – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="865aa-150">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="865aa-151">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="865aa-151">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="865aa-152">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="865aa-152">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="865aa-153">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="865aa-153">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="865aa-154">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="865aa-154">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="865aa-155">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="865aa-155">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="865aa-156">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="865aa-156">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="865aa-157">Anfang-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="865aa-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
