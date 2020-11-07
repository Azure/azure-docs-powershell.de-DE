---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchernexthop
schema: 2.0.0
ms.openlocfilehash: 41c76d78ad27ff889f2dc3e7be254bcc88668023
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850407"
---
# <span data-ttu-id="2e0a4-101">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2e0a4-101">Get-AzureRmNetworkWatcherNextHop</span></span>

## <span data-ttu-id="2e0a4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2e0a4-102">SYNOPSIS</span></span>
<span data-ttu-id="2e0a4-103">Ruft den nächsten Hop von einem virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="2e0a4-103">Gets the next hop from a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e0a4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e0a4-104">SYNTAX</span></span>

### <span data-ttu-id="2e0a4-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="2e0a4-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e0a4-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="2e0a4-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e0a4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2e0a4-107">DESCRIPTION</span></span>
<span data-ttu-id="2e0a4-108">Das Get-AzureRmNetworkWatcherNextHop-Cmdlet ruft den nächsten Hop von einem virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="2e0a4-108">The Get-AzureRmNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="2e0a4-109">Im nächsten Hop können Sie den Typ der Azure-Ressource, die zugehörige IP-Adresse dieser Ressource und die Routingtabellen Regel anzeigen, die für die Route verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="2e0a4-109">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="2e0a4-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2e0a4-110">EXAMPLES</span></span>

### <span data-ttu-id="2e0a4-111">--Beispiel 1: Abrufen des nächsten Hop bei der Kommunikation mit einer Internet-IP--</span><span class="sxs-lookup"><span data-stu-id="2e0a4-111">-- Example 1: Get the Next Hop when communicating with an Internet IP --</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName ContosoResourceGroup -Name VM0
$Nics = Get-AzureRmNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}
Get-AzureRmNetworkWatcherNextHop -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -SourceIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress  -DestinationIPAddress 204.79.197.200


NextHopIpAddress NextHopType RouteTableId
---------------- ----------- ------------
                 Internet    System Route
```

<span data-ttu-id="2e0a4-112">Abrufen des nächsten Hop für ausgehende Kommunikation von der primären Netzwerkschnittstelle des angegebenen virtuellen Vachine zu 204.79.197.200 (www.Bing.com)</span><span class="sxs-lookup"><span data-stu-id="2e0a4-112">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="2e0a4-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="2e0a4-113">PARAMETERS</span></span>

### <span data-ttu-id="2e0a4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2e0a4-114">-AsJob</span></span>
<span data-ttu-id="2e0a4-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2e0a4-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2e0a4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e0a4-116">-DefaultProfile</span></span>
<span data-ttu-id="2e0a4-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2e0a4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e0a4-118">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="2e0a4-118">-DestinationIPAddress</span></span>
<span data-ttu-id="2e0a4-119">Ziel-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="2e0a4-119">Destination IP address.</span></span>

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

### <span data-ttu-id="2e0a4-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2e0a4-120">-NetworkWatcher</span></span>
<span data-ttu-id="2e0a4-121">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="2e0a4-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="2e0a4-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="2e0a4-122">-NetworkWatcherName</span></span>
<span data-ttu-id="2e0a4-123">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="2e0a4-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="2e0a4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e0a4-124">-ResourceGroupName</span></span>
<span data-ttu-id="2e0a4-125">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="2e0a4-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="2e0a4-126">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="2e0a4-126">-SourceIPAddress</span></span>
<span data-ttu-id="2e0a4-127">Quell-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="2e0a4-127">Source IP address.</span></span>

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

### <span data-ttu-id="2e0a4-128">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="2e0a4-128">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="2e0a4-129">Zielnetzwerk-Schnittstellenkennung</span><span class="sxs-lookup"><span data-stu-id="2e0a4-129">Target network interface Id.</span></span>

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

### <span data-ttu-id="2e0a4-130">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="2e0a4-130">-TargetVirtualMachineId</span></span>
<span data-ttu-id="2e0a4-131">Die ID des virtuellen Zielcomputers</span><span class="sxs-lookup"><span data-stu-id="2e0a4-131">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="2e0a4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e0a4-132">CommonParameters</span></span>
<span data-ttu-id="2e0a4-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e0a4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e0a4-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e0a4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e0a4-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2e0a4-135">INPUTS</span></span>

### <span data-ttu-id="2e0a4-136">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2e0a4-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="2e0a4-137">System. String</span><span class="sxs-lookup"><span data-stu-id="2e0a4-137">System.String</span></span>

## <span data-ttu-id="2e0a4-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2e0a4-138">OUTPUTS</span></span>

### <span data-ttu-id="2e0a4-139">Microsoft. Azure. Commands. Network. Models. PSNextHopResult</span><span class="sxs-lookup"><span data-stu-id="2e0a4-139">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="2e0a4-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="2e0a4-140">NOTES</span></span>
<span data-ttu-id="2e0a4-141">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerk-Watcher, weiter, Hop</span><span class="sxs-lookup"><span data-stu-id="2e0a4-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="2e0a4-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2e0a4-142">RELATED LINKS</span></span>

[<span data-ttu-id="2e0a4-143">Neu – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2e0a4-143">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="2e0a4-144">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2e0a4-144">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="2e0a4-145">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2e0a4-145">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="2e0a4-146">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2e0a4-146">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="2e0a4-147">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2e0a4-147">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="2e0a4-148">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2e0a4-148">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="2e0a4-149">Anfang-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2e0a4-149">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="2e0a4-150">Neu – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2e0a4-150">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2e0a4-151">Neu – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2e0a4-151">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="2e0a4-152">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2e0a4-152">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2e0a4-153">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2e0a4-153">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2e0a4-154">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2e0a4-154">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

