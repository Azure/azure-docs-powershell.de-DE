---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 3cb69a6dbf2a08c242d0a49e6d023692663b7f19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498273"
---
# <span data-ttu-id="29c15-101">Stop-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="29c15-101">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="29c15-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="29c15-102">SYNOPSIS</span></span>
<span data-ttu-id="29c15-103">Beenden eines Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="29c15-103">Stop a connection monitor</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29c15-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="29c15-104">SYNTAX</span></span>

### <span data-ttu-id="29c15-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="29c15-105">SetByName (Default)</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29c15-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="29c15-106">SetByResource</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29c15-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="29c15-107">SetByLocation</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29c15-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="29c15-108">SetByResourceId</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29c15-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="29c15-109">SetByInputObject</span></span>
```
Stop-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29c15-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="29c15-110">DESCRIPTION</span></span>
<span data-ttu-id="29c15-111">Das Stop-AzureRmNetworkWatcherConnectionMonitor-Cmdlet beendet den angegebenen Verbindungsmonitor.</span><span class="sxs-lookup"><span data-stu-id="29c15-111">The Stop-AzureRmNetworkWatcherConnectionMonitor cmdlet stops the specified connection monitor.</span></span>

## <span data-ttu-id="29c15-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="29c15-112">EXAMPLES</span></span>

### <span data-ttu-id="29c15-113">Beispiel 1: Beenden eines Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="29c15-113">Example 1: Stop a connection monitor</span></span>
```
PS C:\> Stop-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher $nw -Name cm
```

<span data-ttu-id="29c15-114">In diesem Beispiel wird der vom Namen und Netzwerkmonitor angegebene Verbindungsmonitor beendet</span><span class="sxs-lookup"><span data-stu-id="29c15-114">In this example we stop connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="29c15-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="29c15-115">PARAMETERS</span></span>

### <span data-ttu-id="29c15-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29c15-116">-AsJob</span></span>
<span data-ttu-id="29c15-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="29c15-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="29c15-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29c15-118">-DefaultProfile</span></span>
<span data-ttu-id="29c15-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="29c15-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29c15-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="29c15-120">-InputObject</span></span>
<span data-ttu-id="29c15-121">Connection Monitor-Objekt.</span><span class="sxs-lookup"><span data-stu-id="29c15-121">Connection monitor object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29c15-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="29c15-122">-Location</span></span>
<span data-ttu-id="29c15-123">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="29c15-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="29c15-124">-Name</span><span class="sxs-lookup"><span data-stu-id="29c15-124">-Name</span></span>
<span data-ttu-id="29c15-125">Name des Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="29c15-125">The connection monitor name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29c15-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="29c15-126">-NetworkWatcher</span></span>
<span data-ttu-id="29c15-127">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="29c15-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="29c15-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="29c15-128">-NetworkWatcherName</span></span>
<span data-ttu-id="29c15-129">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="29c15-129">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29c15-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29c15-130">-PassThru</span></span>
<span data-ttu-id="29c15-131">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="29c15-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="29c15-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29c15-132">-ResourceGroupName</span></span>
<span data-ttu-id="29c15-133">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="29c15-133">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29c15-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="29c15-134">-ResourceId</span></span>
<span data-ttu-id="29c15-135">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="29c15-135">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29c15-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="29c15-136">-Confirm</span></span>
<span data-ttu-id="29c15-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="29c15-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29c15-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29c15-138">-WhatIf</span></span>
<span data-ttu-id="29c15-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="29c15-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29c15-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="29c15-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29c15-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29c15-141">CommonParameters</span></span>
<span data-ttu-id="29c15-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29c15-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29c15-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29c15-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29c15-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="29c15-144">INPUTS</span></span>

### <span data-ttu-id="29c15-145">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="29c15-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="29c15-146">Parameter: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="29c15-146">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="29c15-147">System. String</span><span class="sxs-lookup"><span data-stu-id="29c15-147">System.String</span></span>

### <span data-ttu-id="29c15-148">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="29c15-148">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>
<span data-ttu-id="29c15-149">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="29c15-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="29c15-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="29c15-150">OUTPUTS</span></span>

### <span data-ttu-id="29c15-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="29c15-151">System.Boolean</span></span>

## <span data-ttu-id="29c15-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="29c15-152">NOTES</span></span>
<span data-ttu-id="29c15-153">Schlüsselwörter: Azure, azurerm, arm, Ressource, Konnektivität, Verwaltung, Manager, Netzwerk, Netzwerke, Netzwerkmonitor, Verbindungsmonitor</span><span class="sxs-lookup"><span data-stu-id="29c15-153">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="29c15-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="29c15-154">RELATED LINKS</span></span>

[<span data-ttu-id="29c15-155">Neu – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="29c15-155">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="29c15-156">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="29c15-156">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="29c15-157">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="29c15-157">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="29c15-158">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="29c15-158">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="29c15-159">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="29c15-159">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="29c15-160">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="29c15-160">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="29c15-161">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="29c15-161">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="29c15-162">Neu – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="29c15-162">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="29c15-163">Neu – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="29c15-163">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="29c15-164">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="29c15-164">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="29c15-165">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="29c15-165">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="29c15-166">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="29c15-166">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="29c15-167">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="29c15-167">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="29c15-168">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="29c15-168">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="29c15-169">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="29c15-169">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="29c15-170">Satz-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="29c15-170">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="29c15-171">Stopp-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="29c15-171">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="29c15-172">Neu – AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="29c15-172">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="29c15-173">Neu – AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="29c15-173">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>]()

[<span data-ttu-id="29c15-174">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="29c15-174">Test-AzureRmNetworkWatcherIPFlow</span></span>]()

[<span data-ttu-id="29c15-175">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="29c15-175">Test-AzureRmNetworkWatcherConnectivity</span></span>]()

[<span data-ttu-id="29c15-176">Anfang-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="29c15-176">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>]()

[<span data-ttu-id="29c15-177">Anfang-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="29c15-177">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="29c15-178">Satz-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="29c15-178">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>]()

[<span data-ttu-id="29c15-179">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="29c15-179">Get-AzureRMNetworkWatcherReachabilityReport</span></span>]()

[<span data-ttu-id="29c15-180">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="29c15-180">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>]()

[<span data-ttu-id="29c15-181">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="29c15-181">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>]()
