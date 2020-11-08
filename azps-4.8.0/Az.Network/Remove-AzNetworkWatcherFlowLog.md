---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 9906af7da12f76650ebbe45ff764da78c90ef340
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165148"
---
# <span data-ttu-id="a6ef8-101">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="a6ef8-101">Remove-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="a6ef8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a6ef8-102">SYNOPSIS</span></span>
<span data-ttu-id="a6ef8-103">Löscht die angegebene Flow Log-Ressource.</span><span class="sxs-lookup"><span data-stu-id="a6ef8-103">Deletes the specified flow log resource.</span></span>

## <span data-ttu-id="a6ef8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a6ef8-104">SYNTAX</span></span>

### <span data-ttu-id="a6ef8-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a6ef8-105">SetByName (Default)</span></span>
```
Remove-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6ef8-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="a6ef8-106">SetByResource</span></span>
```
Remove-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6ef8-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="a6ef8-107">SetByLocation</span></span>
```
Remove-AzNetworkWatcherFlowLog -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6ef8-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a6ef8-108">SetByResourceId</span></span>
```
Remove-AzNetworkWatcherFlowLog -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6ef8-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="a6ef8-109">SetByInputObject</span></span>
```
Remove-AzNetworkWatcherFlowLog -InputObject <PSFlowLogResource> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6ef8-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a6ef8-110">DESCRIPTION</span></span>
<span data-ttu-id="a6ef8-111">Löscht die angegebene Flow Log-Ressource.</span><span class="sxs-lookup"><span data-stu-id="a6ef8-111">Deletes the specified flow log resource.</span></span>

## <span data-ttu-id="a6ef8-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a6ef8-112">EXAMPLES</span></span>

### <span data-ttu-id="a6ef8-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a6ef8-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkWatcherFlowLog -Location eastus -Name pstest
```

## <span data-ttu-id="a6ef8-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6ef8-114">PARAMETERS</span></span>

### <span data-ttu-id="a6ef8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a6ef8-115">-AsJob</span></span>
<span data-ttu-id="a6ef8-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a6ef8-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a6ef8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6ef8-117">-DefaultProfile</span></span>
<span data-ttu-id="a6ef8-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a6ef8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6ef8-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a6ef8-119">-InputObject</span></span>
<span data-ttu-id="a6ef8-120">Flow Log-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a6ef8-120">Flow log object.</span></span>

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

### <span data-ttu-id="a6ef8-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="a6ef8-121">-Location</span></span>
<span data-ttu-id="a6ef8-122">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="a6ef8-122">Location of the network watcher.</span></span>

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

### <span data-ttu-id="a6ef8-123">-Name</span><span class="sxs-lookup"><span data-stu-id="a6ef8-123">-Name</span></span>
<span data-ttu-id="a6ef8-124">Der Name des Fluss Protokolls.</span><span class="sxs-lookup"><span data-stu-id="a6ef8-124">The flow log name.</span></span>

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

### <span data-ttu-id="a6ef8-125">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a6ef8-125">-NetworkWatcher</span></span>
<span data-ttu-id="a6ef8-126">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="a6ef8-126">The network watcher resource.</span></span>

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

### <span data-ttu-id="a6ef8-127">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a6ef8-127">-NetworkWatcherName</span></span>
<span data-ttu-id="a6ef8-128">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="a6ef8-128">The name of network watcher.</span></span>

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

### <span data-ttu-id="a6ef8-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6ef8-129">-PassThru</span></span>
<span data-ttu-id="a6ef8-130">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="a6ef8-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="a6ef8-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6ef8-131">-ResourceGroupName</span></span>
<span data-ttu-id="a6ef8-132">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="a6ef8-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="a6ef8-133">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a6ef8-133">-ResourceId</span></span>
<span data-ttu-id="a6ef8-134">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="a6ef8-134">Resource ID.</span></span>

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

### <span data-ttu-id="a6ef8-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a6ef8-135">-Confirm</span></span>
<span data-ttu-id="a6ef8-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a6ef8-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6ef8-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6ef8-137">-WhatIf</span></span>
<span data-ttu-id="a6ef8-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a6ef8-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6ef8-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a6ef8-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6ef8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6ef8-140">CommonParameters</span></span>
<span data-ttu-id="a6ef8-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6ef8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6ef8-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6ef8-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6ef8-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a6ef8-143">INPUTS</span></span>

### <span data-ttu-id="a6ef8-144">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a6ef8-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="a6ef8-145">System. String</span><span class="sxs-lookup"><span data-stu-id="a6ef8-145">System.String</span></span>

### <span data-ttu-id="a6ef8-146">Microsoft. Azure. Commands. Network. Models. PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="a6ef8-146">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="a6ef8-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a6ef8-147">OUTPUTS</span></span>

### <span data-ttu-id="a6ef8-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a6ef8-148">System.Boolean</span></span>

## <span data-ttu-id="a6ef8-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="a6ef8-149">NOTES</span></span>

## <span data-ttu-id="a6ef8-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a6ef8-150">RELATED LINKS</span></span>

[<span data-ttu-id="a6ef8-151">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a6ef8-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="a6ef8-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a6ef8-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="a6ef8-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a6ef8-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="a6ef8-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a6ef8-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="a6ef8-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a6ef8-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="a6ef8-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="a6ef8-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="a6ef8-157">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="a6ef8-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="a6ef8-158">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a6ef8-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a6ef8-159">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a6ef8-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="a6ef8-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a6ef8-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a6ef8-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a6ef8-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a6ef8-162">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a6ef8-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a6ef8-163">Neu – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6ef8-163">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="a6ef8-164">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a6ef8-164">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="a6ef8-165">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="a6ef8-165">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="a6ef8-166">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a6ef8-166">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a6ef8-167">Anfang-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a6ef8-167">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a6ef8-168">Satz-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a6ef8-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a6ef8-169">Satz-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="a6ef8-169">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="a6ef8-170">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a6ef8-170">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a6ef8-171">Neu – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a6ef8-171">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a6ef8-172">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="a6ef8-172">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="a6ef8-173">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="a6ef8-173">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="a6ef8-174">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="a6ef8-174">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="a6ef8-175">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="a6ef8-175">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="a6ef8-176">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="a6ef8-176">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="a6ef8-177">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a6ef8-177">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)

[<span data-ttu-id="a6ef8-178">Neu – AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="a6ef8-178">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="a6ef8-179">Satz-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="a6ef8-179">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="a6ef8-180">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="a6ef8-180">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog)
