---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchersecuritygroupview
schema: 2.0.0
ms.openlocfilehash: fad852ff589b2929df83775a2fa955e72663cfa2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848451"
---
# <span data-ttu-id="d6b29-101">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d6b29-101">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="d6b29-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d6b29-102">SYNOPSIS</span></span>
<span data-ttu-id="d6b29-103">Zeigen Sie die konfigurierten und effektiven Netzwerk Sicherheitsgruppen Regeln an, die auf einem virtuellen Computer angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="d6b29-103">View the configured and effective network security group rules applied on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6b29-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6b29-104">SYNTAX</span></span>

### <span data-ttu-id="d6b29-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="d6b29-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6b29-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="d6b29-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6b29-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d6b29-107">DESCRIPTION</span></span>
<span data-ttu-id="d6b29-108">Mit dem Get-AzureRmNetworkWatcherSecurityGroupView können Sie die konfigurierten und effektiven Netzwerk Sicherheitsgruppen Regeln anzeigen, die auf einem virtuellen Computer angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="d6b29-108">The Get-AzureRmNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="d6b29-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d6b29-109">EXAMPLES</span></span>

### <span data-ttu-id="d6b29-110">---Beispiel 1: Erstellen eines Anrufs für eine Sicherheitsgruppen Ansicht auf einem VM----</span><span class="sxs-lookup"><span data-stu-id="d6b29-110">--- Example 1: Make a Security Group View call on a VM ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="d6b29-111">Im obigen Beispiel erhalten wir zunächst den regionalen Netzwerkmonitor und dann einen virtuellen Computer in der Region.</span><span class="sxs-lookup"><span data-stu-id="d6b29-111">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="d6b29-112">Anschließend wird ein Aufruf der Sicherheitsgruppen Ansicht für den angegebenen virtuellen Computer durchführen.</span><span class="sxs-lookup"><span data-stu-id="d6b29-112">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="d6b29-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6b29-113">PARAMETERS</span></span>

### <span data-ttu-id="d6b29-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d6b29-114">-AsJob</span></span>
<span data-ttu-id="d6b29-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d6b29-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d6b29-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6b29-116">-DefaultProfile</span></span>
<span data-ttu-id="d6b29-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d6b29-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6b29-118">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d6b29-118">-NetworkWatcher</span></span>
<span data-ttu-id="d6b29-119">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="d6b29-119">The network watcher resource.</span></span>

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

### <span data-ttu-id="d6b29-120">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d6b29-120">-NetworkWatcherName</span></span>
<span data-ttu-id="d6b29-121">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="d6b29-121">The name of network watcher.</span></span>

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

### <span data-ttu-id="d6b29-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6b29-122">-ResourceGroupName</span></span>
<span data-ttu-id="d6b29-123">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="d6b29-123">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d6b29-124">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="d6b29-124">-TargetVirtualMachineId</span></span>
<span data-ttu-id="d6b29-125">Die Ziel-VM-ID</span><span class="sxs-lookup"><span data-stu-id="d6b29-125">The target VM Id</span></span>

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

### <span data-ttu-id="d6b29-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6b29-126">CommonParameters</span></span>
<span data-ttu-id="d6b29-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6b29-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6b29-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6b29-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6b29-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d6b29-129">INPUTS</span></span>

### <span data-ttu-id="d6b29-130">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d6b29-130">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="d6b29-131">System. String</span><span class="sxs-lookup"><span data-stu-id="d6b29-131">System.String</span></span>

## <span data-ttu-id="d6b29-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d6b29-132">OUTPUTS</span></span>

### <span data-ttu-id="d6b29-133">Microsoft. Azure. Commands. Network. Models. PSViewNsgRules</span><span class="sxs-lookup"><span data-stu-id="d6b29-133">Microsoft.Azure.Commands.Network.Models.PSViewNsgRules</span></span>

## <span data-ttu-id="d6b29-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="d6b29-134">NOTES</span></span>
<span data-ttu-id="d6b29-135">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerk-Watcher, Flow, IP</span><span class="sxs-lookup"><span data-stu-id="d6b29-135">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="d6b29-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d6b29-136">RELATED LINKS</span></span>

[<span data-ttu-id="d6b29-137">Neu – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d6b29-137">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="d6b29-138">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d6b29-138">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="d6b29-139">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d6b29-139">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="d6b29-140">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d6b29-140">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="d6b29-141">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d6b29-141">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="d6b29-142">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d6b29-142">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="d6b29-143">Anfang-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d6b29-143">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="d6b29-144">Neu – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d6b29-144">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d6b29-145">Neu – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d6b29-145">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="d6b29-146">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d6b29-146">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d6b29-147">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d6b29-147">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d6b29-148">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d6b29-148">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

