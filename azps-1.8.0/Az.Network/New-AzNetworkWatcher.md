---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcher.md
ms.openlocfilehash: 30b8fda9c29608759360e396f5dcecde3c9b95d4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660507"
---
# <span data-ttu-id="8102e-101">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8102e-101">New-AzNetworkWatcher</span></span>

## <span data-ttu-id="8102e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8102e-102">SYNOPSIS</span></span>
<span data-ttu-id="8102e-103">Erstellt eine neue Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="8102e-103">Creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="8102e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8102e-104">SYNTAX</span></span>

```
New-AzNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8102e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8102e-105">DESCRIPTION</span></span>
<span data-ttu-id="8102e-106">Das New-AzNetworkWatcher-Cmdlet erstellt eine neue Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="8102e-106">The New-AzNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="8102e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8102e-107">EXAMPLES</span></span>

### <span data-ttu-id="8102e-108">Beispiel 1: Erstellen eines Netzwerkmonitors</span><span class="sxs-lookup"><span data-stu-id="8102e-108">Example 1: Create a Network Watcher</span></span>
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

<span data-ttu-id="8102e-109">In diesem Beispiel wird ein neuer Netzwerkmonitor in einer neu erstellten Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="8102e-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="8102e-110">Beachten Sie, dass pro Abonnement nur ein Netzwerkmonitor pro Region erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="8102e-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="8102e-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="8102e-111">PARAMETERS</span></span>

### <span data-ttu-id="8102e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8102e-112">-DefaultProfile</span></span>
<span data-ttu-id="8102e-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8102e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8102e-114">-Standort</span><span class="sxs-lookup"><span data-stu-id="8102e-114">-Location</span></span>
<span data-ttu-id="8102e-115">Lage.</span><span class="sxs-lookup"><span data-stu-id="8102e-115">Location.</span></span>

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

### <span data-ttu-id="8102e-116">-Name</span><span class="sxs-lookup"><span data-stu-id="8102e-116">-Name</span></span>
<span data-ttu-id="8102e-117">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="8102e-117">The network watcher name.</span></span>

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

### <span data-ttu-id="8102e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8102e-118">-ResourceGroupName</span></span>
<span data-ttu-id="8102e-119">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8102e-119">The resource group name.</span></span>

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

### <span data-ttu-id="8102e-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="8102e-120">-Tag</span></span>
<span data-ttu-id="8102e-121">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="8102e-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8102e-122">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="8102e-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8102e-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8102e-123">-Confirm</span></span>
<span data-ttu-id="8102e-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8102e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8102e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8102e-125">-WhatIf</span></span>
<span data-ttu-id="8102e-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8102e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8102e-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8102e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8102e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8102e-128">CommonParameters</span></span>
<span data-ttu-id="8102e-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8102e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8102e-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8102e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8102e-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8102e-131">INPUTS</span></span>

### <span data-ttu-id="8102e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8102e-132">System.String</span></span>

### <span data-ttu-id="8102e-133">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8102e-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8102e-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8102e-134">OUTPUTS</span></span>

### <span data-ttu-id="8102e-135">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8102e-135">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="8102e-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="8102e-136">NOTES</span></span>
<span data-ttu-id="8102e-137">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke, Netzwerkmonitor</span><span class="sxs-lookup"><span data-stu-id="8102e-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="8102e-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8102e-138">RELATED LINKS</span></span>

[<span data-ttu-id="8102e-139">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8102e-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="8102e-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8102e-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="8102e-141">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8102e-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="8102e-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="8102e-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="8102e-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="8102e-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="8102e-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="8102e-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="8102e-145">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="8102e-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="8102e-146">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8102e-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8102e-147">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="8102e-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="8102e-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8102e-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8102e-149">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8102e-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8102e-150">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8102e-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8102e-151">Neu – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="8102e-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="8102e-152">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="8102e-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="8102e-153">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="8102e-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="8102e-154">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8102e-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8102e-155">Anfang-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8102e-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8102e-156">Satz-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8102e-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8102e-157">Satz-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="8102e-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="8102e-158">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8102e-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8102e-159">Neu – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8102e-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="8102e-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="8102e-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="8102e-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="8102e-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="8102e-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="8102e-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="8102e-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="8102e-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="8102e-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="8102e-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="8102e-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="8102e-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
