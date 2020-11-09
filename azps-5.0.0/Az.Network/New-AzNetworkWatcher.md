---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
ms.openlocfilehash: 7c8f33d8339bb873b713acabd71ca57fe9107383
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301474"
---
# <span data-ttu-id="e8af0-101">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e8af0-101">New-AzNetworkWatcher</span></span>

## <span data-ttu-id="e8af0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e8af0-102">SYNOPSIS</span></span>
<span data-ttu-id="e8af0-103">Erstellt eine neue Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="e8af0-103">Creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="e8af0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8af0-104">SYNTAX</span></span>

```
New-AzNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8af0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e8af0-105">DESCRIPTION</span></span>
<span data-ttu-id="e8af0-106">Das New-AzNetworkWatcher-Cmdlet erstellt eine neue Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="e8af0-106">The New-AzNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="e8af0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e8af0-107">EXAMPLES</span></span>

### <span data-ttu-id="e8af0-108">Beispiel 1: Erstellen eines Netzwerkmonitors</span><span class="sxs-lookup"><span data-stu-id="e8af0-108">Example 1: Create a Network Watcher</span></span>
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

<span data-ttu-id="e8af0-109">In diesem Beispiel wird ein neuer Netzwerkmonitor in einer neu erstellten Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="e8af0-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="e8af0-110">Beachten Sie, dass pro Abonnement nur ein Netzwerkmonitor pro Region erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="e8af0-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="e8af0-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8af0-111">PARAMETERS</span></span>

### <span data-ttu-id="e8af0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8af0-112">-DefaultProfile</span></span>
<span data-ttu-id="e8af0-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e8af0-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8af0-114">-Standort</span><span class="sxs-lookup"><span data-stu-id="e8af0-114">-Location</span></span>
<span data-ttu-id="e8af0-115">Lage.</span><span class="sxs-lookup"><span data-stu-id="e8af0-115">Location.</span></span>

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

### <span data-ttu-id="e8af0-116">-Name</span><span class="sxs-lookup"><span data-stu-id="e8af0-116">-Name</span></span>
<span data-ttu-id="e8af0-117">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="e8af0-117">The network watcher name.</span></span>

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

### <span data-ttu-id="e8af0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8af0-118">-ResourceGroupName</span></span>
<span data-ttu-id="e8af0-119">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="e8af0-119">The resource group name.</span></span>

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

### <span data-ttu-id="e8af0-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="e8af0-120">-Tag</span></span>
<span data-ttu-id="e8af0-121">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="e8af0-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e8af0-122">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="e8af0-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e8af0-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e8af0-123">-Confirm</span></span>
<span data-ttu-id="e8af0-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e8af0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8af0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8af0-125">-WhatIf</span></span>
<span data-ttu-id="e8af0-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e8af0-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8af0-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e8af0-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8af0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8af0-128">CommonParameters</span></span>
<span data-ttu-id="e8af0-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8af0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8af0-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8af0-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8af0-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e8af0-131">INPUTS</span></span>

### <span data-ttu-id="e8af0-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e8af0-132">System.String</span></span>

### <span data-ttu-id="e8af0-133">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e8af0-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e8af0-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e8af0-134">OUTPUTS</span></span>

### <span data-ttu-id="e8af0-135">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e8af0-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="e8af0-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="e8af0-136">NOTES</span></span>
<span data-ttu-id="e8af0-137">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke, Netzwerkmonitor</span><span class="sxs-lookup"><span data-stu-id="e8af0-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="e8af0-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e8af0-138">RELATED LINKS</span></span>

[<span data-ttu-id="e8af0-139">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e8af0-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="e8af0-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e8af0-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="e8af0-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="e8af0-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="e8af0-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="e8af0-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="e8af0-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="e8af0-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="e8af0-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="e8af0-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="e8af0-145">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="e8af0-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="e8af0-146">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e8af0-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e8af0-147">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="e8af0-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="e8af0-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e8af0-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e8af0-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e8af0-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e8af0-150">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e8af0-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="e8af0-151">Neu – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="e8af0-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="e8af0-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="e8af0-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="e8af0-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="e8af0-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="e8af0-154">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e8af0-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e8af0-155">Anfang-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e8af0-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e8af0-156">Satz-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e8af0-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e8af0-157">Satz-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="e8af0-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="e8af0-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e8af0-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e8af0-159">Neu – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e8af0-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="e8af0-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="e8af0-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="e8af0-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="e8af0-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="e8af0-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="e8af0-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="e8af0-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="e8af0-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="e8af0-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="e8af0-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="e8af0-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="e8af0-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
