---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
ms.openlocfilehash: f38250a4beed7eb05f758e17a1d3d17f1d76f86e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400194"
---
# <span data-ttu-id="157b2-101">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="157b2-101">New-AzNetworkWatcher</span></span>

## <span data-ttu-id="157b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="157b2-102">SYNOPSIS</span></span>
<span data-ttu-id="157b2-103">Erstellt eine neue Network Watcher-Ressource.</span><span class="sxs-lookup"><span data-stu-id="157b2-103">Creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="157b2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="157b2-104">SYNTAX</span></span>

```
New-AzNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="157b2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="157b2-105">DESCRIPTION</span></span>
<span data-ttu-id="157b2-106">Das New-AzNetworkWatcher erstellt eine neue Network Watcher-Ressource.</span><span class="sxs-lookup"><span data-stu-id="157b2-106">The New-AzNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="157b2-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="157b2-107">EXAMPLES</span></span>

### <span data-ttu-id="157b2-108">Beispiel 1: Erstellen eines Netzwerk-Watcher-Kontos</span><span class="sxs-lookup"><span data-stu-id="157b2-108">Example 1: Create a Network Watcher</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"7cf1f2fe-8445-4aa7-9bf5-c15347282c39"
Location          : westcentralus
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="157b2-109">In diesem Beispiel wird ein neues Netzwerk-Watcher-System in einer neu erstellten Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="157b2-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="157b2-110">Beachten Sie, dass pro Region und Abonnement nur ein Network Watcher erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="157b2-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="157b2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="157b2-111">PARAMETERS</span></span>

### <span data-ttu-id="157b2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="157b2-112">-DefaultProfile</span></span>
<span data-ttu-id="157b2-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="157b2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="157b2-114">-Location</span><span class="sxs-lookup"><span data-stu-id="157b2-114">-Location</span></span>
<span data-ttu-id="157b2-115">"Ort" aus.</span><span class="sxs-lookup"><span data-stu-id="157b2-115">Location.</span></span>

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

### <span data-ttu-id="157b2-116">-Name</span><span class="sxs-lookup"><span data-stu-id="157b2-116">-Name</span></span>
<span data-ttu-id="157b2-117">Der Name der Netzwerkuhr.</span><span class="sxs-lookup"><span data-stu-id="157b2-117">The network watcher name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="157b2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="157b2-118">-ResourceGroupName</span></span>
<span data-ttu-id="157b2-119">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="157b2-119">The resource group name.</span></span>

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

### <span data-ttu-id="157b2-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="157b2-120">-Tag</span></span>
<span data-ttu-id="157b2-121">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="157b2-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="157b2-122">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="157b2-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="157b2-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="157b2-123">-Confirm</span></span>
<span data-ttu-id="157b2-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="157b2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="157b2-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="157b2-125">-WhatIf</span></span>
<span data-ttu-id="157b2-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="157b2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="157b2-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="157b2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="157b2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="157b2-128">CommonParameters</span></span>
<span data-ttu-id="157b2-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="157b2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="157b2-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="157b2-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="157b2-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="157b2-131">INPUTS</span></span>

### <span data-ttu-id="157b2-132">System.String</span><span class="sxs-lookup"><span data-stu-id="157b2-132">System.String</span></span>

### <span data-ttu-id="157b2-133">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="157b2-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="157b2-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="157b2-134">OUTPUTS</span></span>

### <span data-ttu-id="157b2-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="157b2-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="157b2-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="157b2-136">NOTES</span></span>
<span data-ttu-id="157b2-137">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span><span class="sxs-lookup"><span data-stu-id="157b2-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="157b2-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="157b2-138">RELATED LINKS</span></span>

[<span data-ttu-id="157b2-139">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="157b2-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="157b2-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="157b2-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="157b2-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="157b2-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="157b2-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="157b2-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="157b2-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="157b2-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="157b2-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="157b2-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="157b2-145">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="157b2-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="157b2-146">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="157b2-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="157b2-147">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="157b2-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="157b2-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="157b2-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="157b2-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="157b2-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="157b2-150">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="157b2-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="157b2-151">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="157b2-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="157b2-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="157b2-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="157b2-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="157b2-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="157b2-154">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="157b2-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="157b2-155">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="157b2-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="157b2-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="157b2-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="157b2-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="157b2-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="157b2-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="157b2-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="157b2-159">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="157b2-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="157b2-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="157b2-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="157b2-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="157b2-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="157b2-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="157b2-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="157b2-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="157b2-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="157b2-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="157b2-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="157b2-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="157b2-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
