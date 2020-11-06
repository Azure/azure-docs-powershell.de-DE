---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 7f9417fe4ad6e115e73502e953dfcab965ccd17b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479042"
---
# <span data-ttu-id="1e9f4-101">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1e9f4-101">Remove-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="1e9f4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1e9f4-102">SYNOPSIS</span></span>
<span data-ttu-id="1e9f4-103">Entfernt eine Paket Erfassungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="1e9f4-103">Removes a packet capture resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e9f4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e9f4-104">SYNTAX</span></span>

### <span data-ttu-id="1e9f4-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="1e9f4-105">SetByResource (Default)</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e9f4-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="1e9f4-106">SetByName</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1e9f4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1e9f4-107">DESCRIPTION</span></span>
<span data-ttu-id="1e9f4-108">Die Remove-AzureRmNetworkWatcherPacketCapture entfernt eine Sammlungs Ressource.</span><span class="sxs-lookup"><span data-stu-id="1e9f4-108">The Remove-AzureRmNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="1e9f4-109">Es wird empfohlen, Stop-AzureRmNetworkWatcherPacketCapture aufzurufen, bevor Sie Remove-AzureRmNetworkWatcherPacketCapture aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1e9f4-109">It is recommended to call Stop-AzureRmNetworkWatcherPacketCapture before calling Remove-AzureRmNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="1e9f4-110">Wenn die Paket Aufnahmesitzung ausgeführt wird, wenn Remove-AzureRmNetworkWatcherPacketCapture aufgerufen wird, wird die Paketerfassung möglicherweise nicht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1e9f4-110">If the packet capture session is running when Remove-AzureRmNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="1e9f4-111">Wenn die Sitzung vor dem Entfernen angehalten wird, wird die Cap-Datei, die die Aufnahmedaten enthält, nicht entfernt.</span><span class="sxs-lookup"><span data-stu-id="1e9f4-111">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="1e9f4-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1e9f4-112">EXAMPLES</span></span>

### <span data-ttu-id="1e9f4-113">---Beispiel 1: Entfernen einer Paket Aufnahmesitzung--</span><span class="sxs-lookup"><span data-stu-id="1e9f4-113">--- Example 1: Remove a packet capture session --</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="1e9f4-114">In diesem Beispiel wird eine vorhandene Paket erfassungssitzung mit dem Namen "PacketCaptureTest" entfernt.</span><span class="sxs-lookup"><span data-stu-id="1e9f4-114">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="1e9f4-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e9f4-115">PARAMETERS</span></span>

### <span data-ttu-id="1e9f4-116">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1e9f4-116">-NetworkWatcher</span></span>
<span data-ttu-id="1e9f4-117">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="1e9f4-117">The network watcher resource.</span></span>

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

### <span data-ttu-id="1e9f4-118">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="1e9f4-118">-NetworkWatcherName</span></span>
<span data-ttu-id="1e9f4-119">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="1e9f4-119">The name of network watcher.</span></span>

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

### <span data-ttu-id="1e9f4-120">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="1e9f4-120">-PacketCaptureName</span></span>
<span data-ttu-id="1e9f4-121">Der Name der Paketaufzeichnung.</span><span class="sxs-lookup"><span data-stu-id="1e9f4-121">The packet capture name.</span></span>

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

### <span data-ttu-id="1e9f4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1e9f4-122">-PassThru</span></span>
<span data-ttu-id="1e9f4-123">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="1e9f4-123">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e9f4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e9f4-124">-ResourceGroupName</span></span>
<span data-ttu-id="1e9f4-125">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="1e9f4-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="1e9f4-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1e9f4-126">-Confirm</span></span>
<span data-ttu-id="1e9f4-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1e9f4-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e9f4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e9f4-128">-WhatIf</span></span>
<span data-ttu-id="1e9f4-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1e9f4-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e9f4-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1e9f4-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e9f4-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e9f4-131">-DefaultProfile</span></span>
<span data-ttu-id="1e9f4-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1e9f4-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e9f4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e9f4-133">CommonParameters</span></span>
<span data-ttu-id="1e9f4-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e9f4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e9f4-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e9f4-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e9f4-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1e9f4-136">INPUTS</span></span>

### <span data-ttu-id="1e9f4-137">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1e9f4-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="1e9f4-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1e9f4-138">System.String</span></span>

## <span data-ttu-id="1e9f4-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1e9f4-139">OUTPUTS</span></span>

### <span data-ttu-id="1e9f4-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="1e9f4-140">System.Object</span></span>

## <span data-ttu-id="1e9f4-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="1e9f4-141">NOTES</span></span>
<span data-ttu-id="1e9f4-142">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerkmonitor, Paket, erfassen, Datenverkehr, entfernen</span><span class="sxs-lookup"><span data-stu-id="1e9f4-142">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="1e9f4-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1e9f4-143">RELATED LINKS</span></span>

[<span data-ttu-id="1e9f4-144">Neu – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1e9f4-144">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1e9f4-145">Neu – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="1e9f4-145">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="1e9f4-146">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1e9f4-146">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1e9f4-147">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="1e9f4-147">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="1e9f4-148">Neu – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1e9f4-148">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="1e9f4-149">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1e9f4-149">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="1e9f4-150">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="1e9f4-150">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="1e9f4-151">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="1e9f4-151">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="1e9f4-152">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="1e9f4-152">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="1e9f4-153">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="1e9f4-153">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="1e9f4-154">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="1e9f4-154">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="1e9f4-155">Anfang-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="1e9f4-155">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
