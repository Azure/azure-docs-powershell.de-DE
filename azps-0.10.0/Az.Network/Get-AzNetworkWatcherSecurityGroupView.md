---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: fe315ac4b6c29b8ffd1c82c8045ba9b7a7aab4a0
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841559"
---
# <span data-ttu-id="8c8f3-101">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="8c8f3-101">Get-AzNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="8c8f3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8c8f3-102">SYNOPSIS</span></span>
<span data-ttu-id="8c8f3-103">Zeigen Sie die konfigurierten und effektiven Netzwerk Sicherheitsgruppen Regeln an, die auf einem virtuellen Computer angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="8c8f3-103">View the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="8c8f3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c8f3-104">SYNTAX</span></span>

### <span data-ttu-id="8c8f3-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="8c8f3-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c8f3-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="8c8f3-106">SetByName</span></span>
```
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c8f3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8c8f3-107">DESCRIPTION</span></span>
<span data-ttu-id="8c8f3-108">Mit dem Get-AzNetworkWatcherSecurityGroupView können Sie die konfigurierten und effektiven Netzwerk Sicherheitsgruppen Regeln anzeigen, die auf einem virtuellen Computer angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="8c8f3-108">The Get-AzNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="8c8f3-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8c8f3-109">EXAMPLES</span></span>

### <span data-ttu-id="8c8f3-110">---Beispiel 1: Erstellen eines Anrufs für eine Sicherheitsgruppen Ansicht auf einem VM----</span><span class="sxs-lookup"><span data-stu-id="8c8f3-110">--- Example 1: Make a Security Group View call on a VM ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="8c8f3-111">Im obigen Beispiel erhalten wir zunächst den regionalen Netzwerkmonitor und dann einen virtuellen Computer in der Region.</span><span class="sxs-lookup"><span data-stu-id="8c8f3-111">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="8c8f3-112">Anschließend wird ein Aufruf der Sicherheitsgruppen Ansicht für den angegebenen virtuellen Computer durchführen.</span><span class="sxs-lookup"><span data-stu-id="8c8f3-112">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="8c8f3-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c8f3-113">PARAMETERS</span></span>

### <span data-ttu-id="8c8f3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8c8f3-114">-AsJob</span></span>
<span data-ttu-id="8c8f3-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8c8f3-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8c8f3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c8f3-116">-DefaultProfile</span></span>
<span data-ttu-id="8c8f3-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8c8f3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c8f3-118">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8c8f3-118">-NetworkWatcher</span></span>
<span data-ttu-id="8c8f3-119">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="8c8f3-119">The network watcher resource.</span></span>

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

### <span data-ttu-id="8c8f3-120">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="8c8f3-120">-NetworkWatcherName</span></span>
<span data-ttu-id="8c8f3-121">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="8c8f3-121">The name of network watcher.</span></span>

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

### <span data-ttu-id="8c8f3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c8f3-122">-ResourceGroupName</span></span>
<span data-ttu-id="8c8f3-123">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="8c8f3-123">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="8c8f3-124">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="8c8f3-124">-TargetVirtualMachineId</span></span>
<span data-ttu-id="8c8f3-125">Die Ziel-VM-ID</span><span class="sxs-lookup"><span data-stu-id="8c8f3-125">The target VM Id</span></span>

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

### <span data-ttu-id="8c8f3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c8f3-126">CommonParameters</span></span>
<span data-ttu-id="8c8f3-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c8f3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c8f3-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c8f3-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c8f3-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8c8f3-129">INPUTS</span></span>

### <span data-ttu-id="8c8f3-130">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8c8f3-130">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="8c8f3-131">System. String</span><span class="sxs-lookup"><span data-stu-id="8c8f3-131">System.String</span></span>

## <span data-ttu-id="8c8f3-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8c8f3-132">OUTPUTS</span></span>

### <span data-ttu-id="8c8f3-133">Microsoft. Azure. Commands. Network. Models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="8c8f3-133">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="8c8f3-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="8c8f3-134">NOTES</span></span>
<span data-ttu-id="8c8f3-135">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerk-Watcher, Flow, IP</span><span class="sxs-lookup"><span data-stu-id="8c8f3-135">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="8c8f3-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8c8f3-136">RELATED LINKS</span></span>

[<span data-ttu-id="8c8f3-137">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8c8f3-137">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="8c8f3-138">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8c8f3-138">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="8c8f3-139">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8c8f3-139">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="8c8f3-140">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="8c8f3-140">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="8c8f3-141">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="8c8f3-141">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="8c8f3-142">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="8c8f3-142">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="8c8f3-143">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="8c8f3-143">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="8c8f3-144">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8c8f3-144">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8c8f3-145">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="8c8f3-145">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="8c8f3-146">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8c8f3-146">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8c8f3-147">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8c8f3-147">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8c8f3-148">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8c8f3-148">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

