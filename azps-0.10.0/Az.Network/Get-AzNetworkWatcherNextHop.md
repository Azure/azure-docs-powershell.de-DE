---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
ms.openlocfilehash: 02e24fd35fbe2e5aec5fc8b6ed73d3608d07c5b2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841567"
---
# <span data-ttu-id="f6ccf-101">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="f6ccf-101">Get-AzNetworkWatcherNextHop</span></span>

## <span data-ttu-id="f6ccf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f6ccf-102">SYNOPSIS</span></span>
<span data-ttu-id="f6ccf-103">Ruft den nächsten Hop von einem virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="f6ccf-103">Gets the next hop from a VM.</span></span>

## <span data-ttu-id="f6ccf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6ccf-104">SYNTAX</span></span>

### <span data-ttu-id="f6ccf-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="f6ccf-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6ccf-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="f6ccf-106">SetByName</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6ccf-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f6ccf-107">DESCRIPTION</span></span>
<span data-ttu-id="f6ccf-108">Das Get-AzNetworkWatcherNextHop-Cmdlet ruft den nächsten Hop von einem virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="f6ccf-108">The Get-AzNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="f6ccf-109">Im nächsten Hop können Sie den Typ der Azure-Ressource, die zugehörige IP-Adresse dieser Ressource und die Routingtabellen Regel anzeigen, die für die Route verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="f6ccf-109">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="f6ccf-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f6ccf-110">EXAMPLES</span></span>

### <span data-ttu-id="f6ccf-111">--Beispiel 1: Abrufen des nächsten Hop bei der Kommunikation mit einer Internet-IP--</span><span class="sxs-lookup"><span data-stu-id="f6ccf-111">-- Example 1: Get the Next Hop when communicating with an Internet IP --</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0
$Nics = Get-AzNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}
Get-AzNetworkWatcherNextHop -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -SourceIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress  -DestinationIPAddress 204.79.197.200


NextHopIpAddress NextHopType RouteTableId
---------------- ----------- ------------
                 Internet    System Route
```

<span data-ttu-id="f6ccf-112">Abrufen des nächsten Hop für ausgehende Kommunikation von der primären Netzwerkschnittstelle des angegebenen virtuellen Vachine zu 204.79.197.200 (www.Bing.com)</span><span class="sxs-lookup"><span data-stu-id="f6ccf-112">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="f6ccf-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6ccf-113">PARAMETERS</span></span>

### <span data-ttu-id="f6ccf-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f6ccf-114">-AsJob</span></span>
<span data-ttu-id="f6ccf-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f6ccf-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f6ccf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6ccf-116">-DefaultProfile</span></span>
<span data-ttu-id="f6ccf-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f6ccf-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6ccf-118">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="f6ccf-118">-DestinationIPAddress</span></span>
<span data-ttu-id="f6ccf-119">Ziel-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="f6ccf-119">Destination IP address.</span></span>

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

### <span data-ttu-id="f6ccf-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f6ccf-120">-NetworkWatcher</span></span>
<span data-ttu-id="f6ccf-121">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="f6ccf-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="f6ccf-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="f6ccf-122">-NetworkWatcherName</span></span>
<span data-ttu-id="f6ccf-123">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="f6ccf-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="f6ccf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6ccf-124">-ResourceGroupName</span></span>
<span data-ttu-id="f6ccf-125">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="f6ccf-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="f6ccf-126">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="f6ccf-126">-SourceIPAddress</span></span>
<span data-ttu-id="f6ccf-127">Quell-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="f6ccf-127">Source IP address.</span></span>

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

### <span data-ttu-id="f6ccf-128">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="f6ccf-128">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="f6ccf-129">Zielnetzwerk-Schnittstellenkennung</span><span class="sxs-lookup"><span data-stu-id="f6ccf-129">Target network interface Id.</span></span>

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

### <span data-ttu-id="f6ccf-130">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="f6ccf-130">-TargetVirtualMachineId</span></span>
<span data-ttu-id="f6ccf-131">Die ID des virtuellen Zielcomputers</span><span class="sxs-lookup"><span data-stu-id="f6ccf-131">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="f6ccf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6ccf-132">CommonParameters</span></span>
<span data-ttu-id="f6ccf-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6ccf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6ccf-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6ccf-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6ccf-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f6ccf-135">INPUTS</span></span>

### <span data-ttu-id="f6ccf-136">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f6ccf-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="f6ccf-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f6ccf-137">System.String</span></span>

## <span data-ttu-id="f6ccf-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f6ccf-138">OUTPUTS</span></span>

### <span data-ttu-id="f6ccf-139">Microsoft. Azure. Commands. Network. Models. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="f6ccf-139">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="f6ccf-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="f6ccf-140">NOTES</span></span>
<span data-ttu-id="f6ccf-141">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerk-Watcher, weiter, Hop</span><span class="sxs-lookup"><span data-stu-id="f6ccf-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="f6ccf-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f6ccf-142">RELATED LINKS</span></span>

[<span data-ttu-id="f6ccf-143">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f6ccf-143">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="f6ccf-144">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f6ccf-144">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="f6ccf-145">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f6ccf-145">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="f6ccf-146">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f6ccf-146">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="f6ccf-147">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f6ccf-147">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="f6ccf-148">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f6ccf-148">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="f6ccf-149">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f6ccf-149">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="f6ccf-150">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f6ccf-150">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f6ccf-151">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f6ccf-151">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="f6ccf-152">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f6ccf-152">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f6ccf-153">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f6ccf-153">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f6ccf-154">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f6ccf-154">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

