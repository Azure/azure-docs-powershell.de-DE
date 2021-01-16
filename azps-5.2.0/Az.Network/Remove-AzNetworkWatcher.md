---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcher.md
ms.openlocfilehash: cce361870f6dc65f644264e52b331c209177668f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98301219"
---
# <span data-ttu-id="b8a24-101">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b8a24-101">Remove-AzNetworkWatcher</span></span>

## <span data-ttu-id="b8a24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8a24-102">SYNOPSIS</span></span>
<span data-ttu-id="b8a24-103">Entfernt ein Netzwerk-Watcher-Konto.</span><span class="sxs-lookup"><span data-stu-id="b8a24-103">Removes a Network Watcher.</span></span>

## <span data-ttu-id="b8a24-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b8a24-104">SYNTAX</span></span>

### <span data-ttu-id="b8a24-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="b8a24-105">SetByResource</span></span>
```
Remove-AzNetworkWatcher -NetworkWatcher <PSNetworkWatcher> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8a24-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="b8a24-106">SetByName</span></span>
```
Remove-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8a24-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="b8a24-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcher -Location <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8a24-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b8a24-108">DESCRIPTION</span></span>
<span data-ttu-id="b8a24-109">Mit Remove-AzNetworkWatcher cmdlet wird eine Network Watcher-Ressource entfernt.</span><span class="sxs-lookup"><span data-stu-id="b8a24-109">The Remove-AzNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="b8a24-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b8a24-110">EXAMPLES</span></span>

### <span data-ttu-id="b8a24-111">Beispiel 1: Erstellen und Löschen eines Netzwerk-Watchers</span><span class="sxs-lookup"><span data-stu-id="b8a24-111">Example 1: Create and delete a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="b8a24-112">In diesem Beispiel wird eine Netzwerkuhr in einer Ressourcengruppe erstellt und dann sofort gelöscht.</span><span class="sxs-lookup"><span data-stu-id="b8a24-112">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="b8a24-113">Beachten Sie, dass pro Region und Abonnement nur ein Network Watcher erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="b8a24-113">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="b8a24-114">Verwenden Sie das Kennzeichen "-Force", um die Eingabeaufforderung beim Löschen des virtuellen Netzwerks zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="b8a24-114">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="b8a24-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8a24-115">PARAMETERS</span></span>

### <span data-ttu-id="b8a24-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8a24-116">-AsJob</span></span>
<span data-ttu-id="b8a24-117">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="b8a24-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b8a24-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8a24-118">-DefaultProfile</span></span>
<span data-ttu-id="b8a24-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b8a24-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8a24-120">-Location</span><span class="sxs-lookup"><span data-stu-id="b8a24-120">-Location</span></span>
<span data-ttu-id="b8a24-121">Position der Netzwerk-Watcher.</span><span class="sxs-lookup"><span data-stu-id="b8a24-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="b8a24-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b8a24-122">-Name</span></span>
<span data-ttu-id="b8a24-123">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="b8a24-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8a24-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b8a24-124">-NetworkWatcher</span></span>
<span data-ttu-id="b8a24-125">Die Netzwerk-Watcher-Ressource.</span><span class="sxs-lookup"><span data-stu-id="b8a24-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="b8a24-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b8a24-126">-PassThru</span></span>
<span data-ttu-id="b8a24-127">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="b8a24-127">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="b8a24-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8a24-128">-ResourceGroupName</span></span>
<span data-ttu-id="b8a24-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b8a24-129">The resource group name.</span></span>

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

### <span data-ttu-id="b8a24-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8a24-130">-Confirm</span></span>
<span data-ttu-id="b8a24-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b8a24-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8a24-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b8a24-132">-WhatIf</span></span>
<span data-ttu-id="b8a24-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b8a24-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8a24-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b8a24-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8a24-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8a24-135">CommonParameters</span></span>
<span data-ttu-id="b8a24-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8a24-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8a24-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8a24-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8a24-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b8a24-138">INPUTS</span></span>

### <span data-ttu-id="b8a24-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b8a24-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="b8a24-140">System.String</span><span class="sxs-lookup"><span data-stu-id="b8a24-140">System.String</span></span>

## <span data-ttu-id="b8a24-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b8a24-141">OUTPUTS</span></span>

### <span data-ttu-id="b8a24-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b8a24-142">System.Boolean</span></span>

## <span data-ttu-id="b8a24-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b8a24-143">NOTES</span></span>
<span data-ttu-id="b8a24-144">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span><span class="sxs-lookup"><span data-stu-id="b8a24-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="b8a24-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b8a24-145">RELATED LINKS</span></span>

[<span data-ttu-id="b8a24-146">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b8a24-146">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="b8a24-147">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b8a24-147">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="b8a24-148">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b8a24-148">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="b8a24-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="b8a24-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="b8a24-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="b8a24-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="b8a24-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="b8a24-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="b8a24-152">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="b8a24-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="b8a24-153">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b8a24-153">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b8a24-154">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="b8a24-154">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="b8a24-155">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b8a24-155">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b8a24-156">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b8a24-156">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b8a24-157">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b8a24-157">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b8a24-158">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8a24-158">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="b8a24-159">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="b8a24-159">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="b8a24-160">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="b8a24-160">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="b8a24-161">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b8a24-161">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b8a24-162">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b8a24-162">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b8a24-163">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b8a24-163">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b8a24-164">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="b8a24-164">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="b8a24-165">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b8a24-165">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b8a24-166">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b8a24-166">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="b8a24-167">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="b8a24-167">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="b8a24-168">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="b8a24-168">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="b8a24-169">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="b8a24-169">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="b8a24-170">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="b8a24-170">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="b8a24-171">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="b8a24-171">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="b8a24-172">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="b8a24-172">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
