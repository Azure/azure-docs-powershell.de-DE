---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherIPFlow.md
ms.openlocfilehash: 6e9700f91a9d6f8db5983604a0146f9d864dafd8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504906"
---
# <span data-ttu-id="d34b8-101">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d34b8-101">Test-AzureRmNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="d34b8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d34b8-102">SYNOPSIS</span></span>
<span data-ttu-id="d34b8-103">Gibt zurück, ob das Paket zu oder von einem bestimmten Ziel zugelassen oder abgelehnt wurde.</span><span class="sxs-lookup"><span data-stu-id="d34b8-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d34b8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d34b8-104">SYNTAX</span></span>

### <span data-ttu-id="d34b8-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="d34b8-105">SetByResource (Default)</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d34b8-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="d34b8-106">SetByName</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d34b8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d34b8-107">DESCRIPTION</span></span>
<span data-ttu-id="d34b8-108">Das Test-AzureRmNetworkWatcherIPFlow-Cmdlet für eine angegebene VM-Ressource und ein Paket mit der angegebenen Richtung unter Verwendung von Local und Remote, IP-Adressen und Ports gibt zurück, ob das Paket zugelassen oder verweigert wurde.</span><span class="sxs-lookup"><span data-stu-id="d34b8-108">The Test-AzureRmNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="d34b8-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d34b8-109">EXAMPLES</span></span>

### <span data-ttu-id="d34b8-110">---Beispiel 1: Ausführen von Test-AzureRmNetworkWatcherIPFlow---</span><span class="sxs-lookup"><span data-stu-id="d34b8-110">--- Example 1: Run Test-AzureRmNetworkWatcherIPFlow ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzureRmNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}

Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="d34b8-111">Holen Sie sich den Netzwerk-Watcher in West Central US für dieses Abonnement, und rufen Sie dann die VM und die zugehörigen Netzwerkschnittstellen ab.</span><span class="sxs-lookup"><span data-stu-id="d34b8-111">Get's the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="d34b8-112">Dann wird für die erste Netzwerkschnittstelle Test-AzureRmNetworkWatcherIPFlow mit der ersten IP-Adresse von der ersten Netzwerkschnittstelle für eine ausgehende Verbindung mit einer IP im Internet ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d34b8-112">Then for the first Network Interface, runs Test-AzureRmNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="d34b8-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d34b8-113">PARAMETERS</span></span>

### <span data-ttu-id="d34b8-114">-Richtung</span><span class="sxs-lookup"><span data-stu-id="d34b8-114">-Direction</span></span>
<span data-ttu-id="d34b8-115">Richtung.</span><span class="sxs-lookup"><span data-stu-id="d34b8-115">Direction.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Inbound, Outbound

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d34b8-116">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="d34b8-116">-LocalIPAddress</span></span>
<span data-ttu-id="d34b8-117">Lokale IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="d34b8-117">Local IP Address.</span></span>

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

### <span data-ttu-id="d34b8-118">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="d34b8-118">-LocalPort</span></span>
<span data-ttu-id="d34b8-119">Lokaler Port.</span><span class="sxs-lookup"><span data-stu-id="d34b8-119">Local Port.</span></span>

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

### <span data-ttu-id="d34b8-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d34b8-120">-NetworkWatcher</span></span>
<span data-ttu-id="d34b8-121">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="d34b8-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="d34b8-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d34b8-122">-NetworkWatcherName</span></span>
<span data-ttu-id="d34b8-123">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="d34b8-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="d34b8-124">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="d34b8-124">-Protocol</span></span>
<span data-ttu-id="d34b8-125">Protokoll.</span><span class="sxs-lookup"><span data-stu-id="d34b8-125">Protocol.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d34b8-126">-Remote</span><span class="sxs-lookup"><span data-stu-id="d34b8-126">-RemoteIPAddress</span></span>
<span data-ttu-id="d34b8-127">Remote-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="d34b8-127">Remote IP Address.</span></span>

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

### <span data-ttu-id="d34b8-128">-Remoteport</span><span class="sxs-lookup"><span data-stu-id="d34b8-128">-RemotePort</span></span>
<span data-ttu-id="d34b8-129">Remote-Port.</span><span class="sxs-lookup"><span data-stu-id="d34b8-129">Remote port.</span></span>

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

### <span data-ttu-id="d34b8-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d34b8-130">-ResourceGroupName</span></span>
<span data-ttu-id="d34b8-131">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="d34b8-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d34b8-132">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="d34b8-132">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="d34b8-133">Zielnetzwerk-Schnittstellenkennung</span><span class="sxs-lookup"><span data-stu-id="d34b8-133">Target network interface Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d34b8-134">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="d34b8-134">-TargetVirtualMachineId</span></span>
<span data-ttu-id="d34b8-135">Die ID des virtuellen Zielcomputers</span><span class="sxs-lookup"><span data-stu-id="d34b8-135">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="d34b8-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d34b8-136">-DefaultProfile</span></span>
<span data-ttu-id="d34b8-137">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d34b8-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d34b8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d34b8-138">CommonParameters</span></span>
<span data-ttu-id="d34b8-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d34b8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d34b8-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d34b8-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d34b8-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d34b8-141">INPUTS</span></span>

### <span data-ttu-id="d34b8-142">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d34b8-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="d34b8-143">System. String</span><span class="sxs-lookup"><span data-stu-id="d34b8-143">System.String</span></span>

## <span data-ttu-id="d34b8-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d34b8-144">OUTPUTS</span></span>

### <span data-ttu-id="d34b8-145">Microsoft. Azure. Commands. Network. Models. PSIPFlowVerifyResult</span><span class="sxs-lookup"><span data-stu-id="d34b8-145">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="d34b8-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="d34b8-146">NOTES</span></span>
<span data-ttu-id="d34b8-147">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerk-Watcher, Flow, IP</span><span class="sxs-lookup"><span data-stu-id="d34b8-147">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="d34b8-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d34b8-148">RELATED LINKS</span></span>

[<span data-ttu-id="d34b8-149">Neu – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d34b8-149">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="d34b8-150">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d34b8-150">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="d34b8-151">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d34b8-151">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="d34b8-152">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d34b8-152">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="d34b8-153">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d34b8-153">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d34b8-154">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d34b8-154">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="d34b8-155">Anfang-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d34b8-155">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="d34b8-156">Neu – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d34b8-156">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d34b8-157">Neu – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d34b8-157">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="d34b8-158">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d34b8-158">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d34b8-159">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d34b8-159">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d34b8-160">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d34b8-160">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)
