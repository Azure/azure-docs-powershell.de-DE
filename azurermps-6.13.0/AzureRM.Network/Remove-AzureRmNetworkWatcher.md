---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcher.md
ms.openlocfilehash: a242c1cbeda2a110f7bb58e8c320f2e9b4d60ac8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503525"
---
# <span data-ttu-id="52e5c-101">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="52e5c-101">Remove-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="52e5c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="52e5c-102">SYNOPSIS</span></span>
<span data-ttu-id="52e5c-103">Entfernt einen Netzwerkmonitor.</span><span class="sxs-lookup"><span data-stu-id="52e5c-103">Removes a Network Watcher.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52e5c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="52e5c-104">SYNTAX</span></span>

### <span data-ttu-id="52e5c-105">SetByResource</span><span class="sxs-lookup"><span data-stu-id="52e5c-105">SetByResource</span></span>
```
Remove-AzureRmNetworkWatcher -NetworkWatcher <PSNetworkWatcher> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52e5c-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="52e5c-106">SetByName</span></span>
```
Remove-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52e5c-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="52e5c-107">SetByLocation</span></span>
```
Remove-AzureRmNetworkWatcher -Location <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52e5c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="52e5c-108">DESCRIPTION</span></span>
<span data-ttu-id="52e5c-109">Das Remove-AzureRmNetworkWatcher-Cmdlet entfernt eine Network Watcher-Ressource.</span><span class="sxs-lookup"><span data-stu-id="52e5c-109">The Remove-AzureRmNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="52e5c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="52e5c-110">EXAMPLES</span></span>

### <span data-ttu-id="52e5c-111">Beispiel 1: Erstellen und Löschen eines Netzwerkmonitors</span><span class="sxs-lookup"><span data-stu-id="52e5c-111">Example 1: Create and delete a Network Watcher</span></span>
```
New-AzureRmResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="52e5c-112">In diesem Beispiel wird ein Netzwerkmonitor in einer Ressourcengruppe erstellt und anschließend sofort gelöscht.</span><span class="sxs-lookup"><span data-stu-id="52e5c-112">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="52e5c-113">Beachten Sie, dass pro Abonnement nur ein Netzwerkmonitor pro Region erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="52e5c-113">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="52e5c-114">Verwenden Sie das Flag-Force, um die Eingabeaufforderung beim Löschen des virtuellen Netzwerks zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="52e5c-114">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="52e5c-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="52e5c-115">PARAMETERS</span></span>

### <span data-ttu-id="52e5c-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52e5c-116">-AsJob</span></span>
<span data-ttu-id="52e5c-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="52e5c-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="52e5c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52e5c-118">-DefaultProfile</span></span>
<span data-ttu-id="52e5c-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="52e5c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52e5c-120">-Standort</span><span class="sxs-lookup"><span data-stu-id="52e5c-120">-Location</span></span>
<span data-ttu-id="52e5c-121">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="52e5c-121">Location of the network watcher.</span></span>

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

### <span data-ttu-id="52e5c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="52e5c-122">-Name</span></span>
<span data-ttu-id="52e5c-123">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="52e5c-123">The resource name.</span></span>

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

### <span data-ttu-id="52e5c-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="52e5c-124">-NetworkWatcher</span></span>
<span data-ttu-id="52e5c-125">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="52e5c-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="52e5c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52e5c-126">-PassThru</span></span>
<span data-ttu-id="52e5c-127">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="52e5c-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="52e5c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52e5c-128">-ResourceGroupName</span></span>
<span data-ttu-id="52e5c-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="52e5c-129">The resource group name.</span></span>

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

### <span data-ttu-id="52e5c-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="52e5c-130">-Confirm</span></span>
<span data-ttu-id="52e5c-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="52e5c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52e5c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52e5c-132">-WhatIf</span></span>
<span data-ttu-id="52e5c-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="52e5c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52e5c-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="52e5c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52e5c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52e5c-135">CommonParameters</span></span>
<span data-ttu-id="52e5c-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52e5c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52e5c-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52e5c-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52e5c-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="52e5c-138">INPUTS</span></span>

### <span data-ttu-id="52e5c-139">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="52e5c-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="52e5c-140">Parameter: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="52e5c-140">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="52e5c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="52e5c-141">System.String</span></span>
<span data-ttu-id="52e5c-142">Parameter: Name (ByValue)</span><span class="sxs-lookup"><span data-stu-id="52e5c-142">Parameters: Name (ByValue)</span></span>

## <span data-ttu-id="52e5c-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="52e5c-143">OUTPUTS</span></span>

### <span data-ttu-id="52e5c-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="52e5c-144">System.Boolean</span></span>

## <span data-ttu-id="52e5c-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="52e5c-145">NOTES</span></span>
<span data-ttu-id="52e5c-146">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke, Netzwerkmonitor</span><span class="sxs-lookup"><span data-stu-id="52e5c-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="52e5c-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="52e5c-147">RELATED LINKS</span></span>

[<span data-ttu-id="52e5c-148">Neu – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="52e5c-148">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="52e5c-149">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="52e5c-149">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="52e5c-150">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="52e5c-150">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="52e5c-151">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="52e5c-151">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="52e5c-152">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="52e5c-152">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="52e5c-153">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="52e5c-153">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="52e5c-154">Anfang-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="52e5c-154">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="52e5c-155">Neu – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="52e5c-155">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="52e5c-156">Neu – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="52e5c-156">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="52e5c-157">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="52e5c-157">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="52e5c-158">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="52e5c-158">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="52e5c-159">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="52e5c-159">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="52e5c-160">Neu – AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="52e5c-160">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="52e5c-161">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="52e5c-161">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="52e5c-162">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="52e5c-162">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="52e5c-163">Stopp-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="52e5c-163">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="52e5c-164">Anfang-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="52e5c-164">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="52e5c-165">Satz-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="52e5c-165">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="52e5c-166">Satz-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="52e5c-166">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="52e5c-167">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="52e5c-167">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="52e5c-168">Neu – AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="52e5c-168">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="52e5c-169">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="52e5c-169">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="52e5c-170">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="52e5c-170">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="52e5c-171">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="52e5c-171">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="52e5c-172">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="52e5c-172">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="52e5c-173">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="52e5c-173">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="52e5c-174">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="52e5c-174">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
