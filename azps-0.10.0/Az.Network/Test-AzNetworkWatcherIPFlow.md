---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcheripflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
ms.openlocfilehash: 307bb2c954526b744f31763f0d3a09d0163c8057
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843508"
---
# <span data-ttu-id="f0b72-101">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f0b72-101">Test-AzNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="f0b72-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f0b72-102">SYNOPSIS</span></span>
<span data-ttu-id="f0b72-103">Gibt zurück, ob das Paket zu oder von einem bestimmten Ziel zugelassen oder abgelehnt wurde.</span><span class="sxs-lookup"><span data-stu-id="f0b72-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

## <span data-ttu-id="f0b72-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0b72-104">SYNTAX</span></span>

### <span data-ttu-id="f0b72-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="f0b72-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0b72-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="f0b72-106">SetByName</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0b72-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f0b72-107">DESCRIPTION</span></span>
<span data-ttu-id="f0b72-108">Das Test-AzNetworkWatcherIPFlow-Cmdlet für eine angegebene VM-Ressource und ein Paket mit der angegebenen Richtung unter Verwendung von Local und Remote, IP-Adressen und Ports gibt zurück, ob das Paket zugelassen oder verweigert wurde.</span><span class="sxs-lookup"><span data-stu-id="f0b72-108">The Test-AzNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="f0b72-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f0b72-109">EXAMPLES</span></span>

### <span data-ttu-id="f0b72-110">---Beispiel 1: Ausführen von Test-AzNetworkWatcherIPFlow---</span><span class="sxs-lookup"><span data-stu-id="f0b72-110">--- Example 1: Run Test-AzNetworkWatcherIPFlow ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}

Test-AzNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="f0b72-111">Holen Sie sich den Netzwerk-Watcher in West Central US für dieses Abonnement, und rufen Sie dann die VM und die zugehörigen Netzwerkschnittstellen ab.</span><span class="sxs-lookup"><span data-stu-id="f0b72-111">Get's the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="f0b72-112">Dann wird für die erste Netzwerkschnittstelle Test-AzNetworkWatcherIPFlow mit der ersten IP-Adresse von der ersten Netzwerkschnittstelle für eine ausgehende Verbindung mit einer IP im Internet ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f0b72-112">Then for the first Network Interface, runs Test-AzNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="f0b72-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f0b72-113">PARAMETERS</span></span>

### <span data-ttu-id="f0b72-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f0b72-114">-AsJob</span></span>
<span data-ttu-id="f0b72-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f0b72-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f0b72-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0b72-116">-DefaultProfile</span></span>
<span data-ttu-id="f0b72-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f0b72-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0b72-118">-Richtung</span><span class="sxs-lookup"><span data-stu-id="f0b72-118">-Direction</span></span>
<span data-ttu-id="f0b72-119">Richtung.</span><span class="sxs-lookup"><span data-stu-id="f0b72-119">Direction.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Inbound, Outbound

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0b72-120">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="f0b72-120">-LocalIPAddress</span></span>
<span data-ttu-id="f0b72-121">Lokale IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="f0b72-121">Local IP Address.</span></span>

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

### <span data-ttu-id="f0b72-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="f0b72-122">-LocalPort</span></span>
<span data-ttu-id="f0b72-123">Lokaler Port.</span><span class="sxs-lookup"><span data-stu-id="f0b72-123">Local Port.</span></span>

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

### <span data-ttu-id="f0b72-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f0b72-124">-NetworkWatcher</span></span>
<span data-ttu-id="f0b72-125">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="f0b72-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="f0b72-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="f0b72-126">-NetworkWatcherName</span></span>
<span data-ttu-id="f0b72-127">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="f0b72-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="f0b72-128">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="f0b72-128">-Protocol</span></span>
<span data-ttu-id="f0b72-129">Protokoll.</span><span class="sxs-lookup"><span data-stu-id="f0b72-129">Protocol.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0b72-130">-Remote</span><span class="sxs-lookup"><span data-stu-id="f0b72-130">-RemoteIPAddress</span></span>
<span data-ttu-id="f0b72-131">Remote-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="f0b72-131">Remote IP Address.</span></span>

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

### <span data-ttu-id="f0b72-132">-Remoteport</span><span class="sxs-lookup"><span data-stu-id="f0b72-132">-RemotePort</span></span>
<span data-ttu-id="f0b72-133">Remote-Port.</span><span class="sxs-lookup"><span data-stu-id="f0b72-133">Remote port.</span></span>

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

### <span data-ttu-id="f0b72-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0b72-134">-ResourceGroupName</span></span>
<span data-ttu-id="f0b72-135">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="f0b72-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="f0b72-136">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="f0b72-136">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="f0b72-137">Zielnetzwerk-Schnittstellenkennung</span><span class="sxs-lookup"><span data-stu-id="f0b72-137">Target network interface Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0b72-138">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="f0b72-138">-TargetVirtualMachineId</span></span>
<span data-ttu-id="f0b72-139">Die ID des virtuellen Zielcomputers</span><span class="sxs-lookup"><span data-stu-id="f0b72-139">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="f0b72-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0b72-140">CommonParameters</span></span>
<span data-ttu-id="f0b72-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0b72-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0b72-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0b72-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0b72-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f0b72-143">INPUTS</span></span>

### <span data-ttu-id="f0b72-144">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f0b72-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="f0b72-145">System. String</span><span class="sxs-lookup"><span data-stu-id="f0b72-145">System.String</span></span>

## <span data-ttu-id="f0b72-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f0b72-146">OUTPUTS</span></span>

### <span data-ttu-id="f0b72-147">Microsoft. Azure. Commands. Network. Models. PSIPFlowVerifyResult</span><span class="sxs-lookup"><span data-stu-id="f0b72-147">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="f0b72-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="f0b72-148">NOTES</span></span>
<span data-ttu-id="f0b72-149">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerk-Watcher, Flow, IP</span><span class="sxs-lookup"><span data-stu-id="f0b72-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="f0b72-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f0b72-150">RELATED LINKS</span></span>

[<span data-ttu-id="f0b72-151">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f0b72-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="f0b72-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f0b72-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="f0b72-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f0b72-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="f0b72-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f0b72-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="f0b72-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f0b72-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="f0b72-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f0b72-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="f0b72-157">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f0b72-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="f0b72-158">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f0b72-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f0b72-159">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f0b72-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="f0b72-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f0b72-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f0b72-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f0b72-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f0b72-162">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f0b72-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)
