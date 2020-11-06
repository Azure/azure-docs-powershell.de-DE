---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: 9fe23ea5fa9bef544feae6112879cb1be6eeae7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479501"
---
# <span data-ttu-id="6ff0a-101">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="6ff0a-101">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="6ff0a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6ff0a-102">SYNOPSIS</span></span>
<span data-ttu-id="6ff0a-103">Zeigen Sie die konfigurierten und effektiven Netzwerk Sicherheitsgruppen Regeln an, die auf einem virtuellen Computer angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="6ff0a-103">View the configured and effective network security group rules applied on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ff0a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ff0a-104">SYNTAX</span></span>

### <span data-ttu-id="6ff0a-105">SetByResource (Standard)</span><span class="sxs-lookup"><span data-stu-id="6ff0a-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ff0a-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="6ff0a-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ff0a-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="6ff0a-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -Location <String> -TargetVirtualMachineId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ff0a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6ff0a-108">DESCRIPTION</span></span>
<span data-ttu-id="6ff0a-109">Mit dem Get-AzureRmNetworkWatcherSecurityGroupView können Sie die konfigurierten und effektiven Netzwerk Sicherheitsgruppen Regeln anzeigen, die auf einem virtuellen Computer angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="6ff0a-109">The Get-AzureRmNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="6ff0a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6ff0a-110">EXAMPLES</span></span>

### <span data-ttu-id="6ff0a-111">Beispiel 1: Erstellen eines Anrufs einer Sicherheitsgruppe auf einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="6ff0a-111">Example 1: Make a Security Group View call on a VM</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="6ff0a-112">Im obigen Beispiel erhalten wir zunächst den regionalen Netzwerkmonitor und dann einen virtuellen Computer in der Region.</span><span class="sxs-lookup"><span data-stu-id="6ff0a-112">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="6ff0a-113">Anschließend wird ein Aufruf der Sicherheitsgruppen Ansicht für den angegebenen virtuellen Computer durchführen.</span><span class="sxs-lookup"><span data-stu-id="6ff0a-113">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="6ff0a-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ff0a-114">PARAMETERS</span></span>

### <span data-ttu-id="6ff0a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ff0a-115">-AsJob</span></span>
<span data-ttu-id="6ff0a-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="6ff0a-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ff0a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ff0a-117">-DefaultProfile</span></span>
<span data-ttu-id="6ff0a-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6ff0a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ff0a-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="6ff0a-119">-Location</span></span>
<span data-ttu-id="6ff0a-120">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="6ff0a-120">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ff0a-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6ff0a-121">-NetworkWatcher</span></span>
<span data-ttu-id="6ff0a-122">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="6ff0a-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="6ff0a-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="6ff0a-123">-NetworkWatcherName</span></span>
<span data-ttu-id="6ff0a-124">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="6ff0a-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="6ff0a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ff0a-125">-ResourceGroupName</span></span>
<span data-ttu-id="6ff0a-126">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="6ff0a-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="6ff0a-127">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="6ff0a-127">-TargetVirtualMachineId</span></span>
<span data-ttu-id="6ff0a-128">Die Ziel-VM-ID</span><span class="sxs-lookup"><span data-stu-id="6ff0a-128">The target VM Id</span></span>

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

### <span data-ttu-id="6ff0a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ff0a-129">CommonParameters</span></span>
<span data-ttu-id="6ff0a-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ff0a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ff0a-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ff0a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ff0a-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6ff0a-132">INPUTS</span></span>

### <span data-ttu-id="6ff0a-133">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6ff0a-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="6ff0a-134">Parameter: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6ff0a-134">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="6ff0a-135">System. String</span><span class="sxs-lookup"><span data-stu-id="6ff0a-135">System.String</span></span>
<span data-ttu-id="6ff0a-136">Parameter: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6ff0a-136">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="6ff0a-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6ff0a-137">OUTPUTS</span></span>

### <span data-ttu-id="6ff0a-138">Microsoft. Azure. Commands. Network. Models. PSSecurityGroupViewResult</span><span class="sxs-lookup"><span data-stu-id="6ff0a-138">Microsoft.Azure.Commands.Network.Models.PSSecurityGroupViewResult</span></span>

## <span data-ttu-id="6ff0a-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="6ff0a-139">NOTES</span></span>
<span data-ttu-id="6ff0a-140">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerk-Watcher, Flow, IP</span><span class="sxs-lookup"><span data-stu-id="6ff0a-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="6ff0a-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6ff0a-141">RELATED LINKS</span></span>

[<span data-ttu-id="6ff0a-142">Neu – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6ff0a-142">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="6ff0a-143">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6ff0a-143">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="6ff0a-144">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6ff0a-144">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="6ff0a-145">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="6ff0a-145">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="6ff0a-146">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="6ff0a-146">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="6ff0a-147">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="6ff0a-147">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="6ff0a-148">Anfang-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="6ff0a-148">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="6ff0a-149">Neu – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6ff0a-149">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6ff0a-150">Neu – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="6ff0a-150">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="6ff0a-151">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6ff0a-151">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6ff0a-152">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6ff0a-152">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6ff0a-153">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6ff0a-153">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6ff0a-154">Neu – AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ff0a-154">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="6ff0a-155">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="6ff0a-155">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="6ff0a-156">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="6ff0a-156">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="6ff0a-157">Stopp-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6ff0a-157">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6ff0a-158">Anfang-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6ff0a-158">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6ff0a-159">Satz-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6ff0a-159">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6ff0a-160">Satz-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="6ff0a-160">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="6ff0a-161">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6ff0a-161">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6ff0a-162">Neu – AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6ff0a-162">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="6ff0a-163">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="6ff0a-163">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="6ff0a-164">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="6ff0a-164">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="6ff0a-165">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="6ff0a-165">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="6ff0a-166">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="6ff0a-166">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="6ff0a-167">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="6ff0a-167">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="6ff0a-168">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="6ff0a-168">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
