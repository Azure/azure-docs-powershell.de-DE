---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 5c8532502e4e74b94a9d0c1e252c8d1cea9ddad8
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398595"
---
# <span data-ttu-id="87ee7-101">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="87ee7-101">Remove-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="87ee7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87ee7-102">SYNOPSIS</span></span>
<span data-ttu-id="87ee7-103">Löscht die angegebene Flussprotokollressource.</span><span class="sxs-lookup"><span data-stu-id="87ee7-103">Deletes the specified flow log resource.</span></span>

## <span data-ttu-id="87ee7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="87ee7-104">SYNTAX</span></span>

### <span data-ttu-id="87ee7-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="87ee7-105">SetByName (Default)</span></span>
```
Remove-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87ee7-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="87ee7-106">SetByResource</span></span>
```
Remove-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87ee7-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="87ee7-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherFlowLog -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87ee7-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="87ee7-108">SetByResourceId</span></span>
```
Remove-AzNetworkWatcherFlowLog -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87ee7-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="87ee7-109">SetByInputObject</span></span>
```
Remove-AzNetworkWatcherFlowLog -InputObject <PSFlowLogResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87ee7-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="87ee7-110">DESCRIPTION</span></span>
<span data-ttu-id="87ee7-111">Löscht die angegebene Flussprotokollressource.</span><span class="sxs-lookup"><span data-stu-id="87ee7-111">Deletes the specified flow log resource.</span></span>

## <span data-ttu-id="87ee7-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="87ee7-112">EXAMPLES</span></span>

### <span data-ttu-id="87ee7-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="87ee7-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkWatcherFlowLog -Location eastus -Name pstest
```

## <span data-ttu-id="87ee7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87ee7-114">PARAMETERS</span></span>

### <span data-ttu-id="87ee7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="87ee7-115">-AsJob</span></span>
<span data-ttu-id="87ee7-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="87ee7-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="87ee7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87ee7-117">-DefaultProfile</span></span>
<span data-ttu-id="87ee7-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="87ee7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87ee7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87ee7-119">-InputObject</span></span>
<span data-ttu-id="87ee7-120">Flussprotokollobjekt.</span><span class="sxs-lookup"><span data-stu-id="87ee7-120">Flow log object.</span></span>

```yaml
Type: PSFlowLogResource
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87ee7-121">-Location</span><span class="sxs-lookup"><span data-stu-id="87ee7-121">-Location</span></span>
<span data-ttu-id="87ee7-122">Speicherort der Netzwerk-Watcher.</span><span class="sxs-lookup"><span data-stu-id="87ee7-122">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87ee7-123">-Name</span><span class="sxs-lookup"><span data-stu-id="87ee7-123">-Name</span></span>
<span data-ttu-id="87ee7-124">Der Name des Flussprotokolls.</span><span class="sxs-lookup"><span data-stu-id="87ee7-124">The flow log name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: FlowLogName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87ee7-125">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="87ee7-125">-NetworkWatcher</span></span>
<span data-ttu-id="87ee7-126">Die Netzwerk-Watcher-Ressource.</span><span class="sxs-lookup"><span data-stu-id="87ee7-126">The network watcher resource.</span></span>

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

### <span data-ttu-id="87ee7-127">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="87ee7-127">-NetworkWatcherName</span></span>
<span data-ttu-id="87ee7-128">Der Name der Netzwerk-Watcher.</span><span class="sxs-lookup"><span data-stu-id="87ee7-128">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87ee7-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="87ee7-129">-PassThru</span></span>
<span data-ttu-id="87ee7-130">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="87ee7-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="87ee7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87ee7-131">-ResourceGroupName</span></span>
<span data-ttu-id="87ee7-132">Der Name der Ressourcengruppe "Netzwerk-Watcher".</span><span class="sxs-lookup"><span data-stu-id="87ee7-132">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87ee7-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87ee7-133">-ResourceId</span></span>
<span data-ttu-id="87ee7-134">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="87ee7-134">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87ee7-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="87ee7-135">-Confirm</span></span>
<span data-ttu-id="87ee7-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="87ee7-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87ee7-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="87ee7-137">-WhatIf</span></span>
<span data-ttu-id="87ee7-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="87ee7-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87ee7-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="87ee7-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87ee7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87ee7-140">CommonParameters</span></span>
<span data-ttu-id="87ee7-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87ee7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87ee7-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="87ee7-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87ee7-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="87ee7-143">INPUTS</span></span>

### <span data-ttu-id="87ee7-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="87ee7-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="87ee7-145">System.String</span><span class="sxs-lookup"><span data-stu-id="87ee7-145">System.String</span></span>

### <span data-ttu-id="87ee7-146">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="87ee7-146">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="87ee7-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="87ee7-147">OUTPUTS</span></span>

### <span data-ttu-id="87ee7-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="87ee7-148">System.Boolean</span></span>

## <span data-ttu-id="87ee7-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="87ee7-149">NOTES</span></span>

## <span data-ttu-id="87ee7-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="87ee7-150">RELATED LINKS</span></span>

[<span data-ttu-id="87ee7-151">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="87ee7-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="87ee7-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="87ee7-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="87ee7-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="87ee7-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="87ee7-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="87ee7-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="87ee7-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="87ee7-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="87ee7-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="87ee7-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="87ee7-157">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="87ee7-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="87ee7-158">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="87ee7-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="87ee7-159">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="87ee7-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="87ee7-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="87ee7-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="87ee7-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="87ee7-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="87ee7-162">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="87ee7-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="87ee7-163">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="87ee7-163">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="87ee7-164">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="87ee7-164">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="87ee7-165">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="87ee7-165">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="87ee7-166">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="87ee7-166">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="87ee7-167">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="87ee7-167">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="87ee7-168">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="87ee7-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="87ee7-169">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="87ee7-169">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="87ee7-170">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="87ee7-170">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="87ee7-171">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="87ee7-171">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="87ee7-172">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="87ee7-172">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="87ee7-173">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="87ee7-173">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="87ee7-174">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="87ee7-174">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="87ee7-175">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="87ee7-175">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="87ee7-176">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="87ee7-176">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="87ee7-177">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="87ee7-177">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="87ee7-178">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="87ee7-178">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="87ee7-179">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="87ee7-179">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="87ee7-180">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="87ee7-180">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog.md)
