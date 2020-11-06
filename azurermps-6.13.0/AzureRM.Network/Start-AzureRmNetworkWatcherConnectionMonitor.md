---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: 7c32c58167336fc032e543261e237430de36653c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498277"
---
# <span data-ttu-id="a3a3f-101">Start-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a3a3f-101">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>

## <span data-ttu-id="a3a3f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a3a3f-102">SYNOPSIS</span></span>
<span data-ttu-id="a3a3f-103">Starten eines Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="a3a3f-103">Start a connection monitor</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3a3f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3a3f-104">SYNTAX</span></span>

### <span data-ttu-id="a3a3f-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a3a3f-105">SetByName (Default)</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String>
 -Name <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a3a3f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="a3a3f-106">SetByResource</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3a3f-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="a3a3f-107">SetByLocation</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -Location <String> -Name <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3a3f-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="a3a3f-108">SetByResourceId</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3a3f-109">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="a3a3f-109">SetByInputObject</span></span>
```
Start-AzureRmNetworkWatcherConnectionMonitor -InputObject <PSConnectionMonitorResult> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3a3f-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a3a3f-110">DESCRIPTION</span></span>
<span data-ttu-id="a3a3f-111">Mit dem Start-AzureRmNetworkWatcherConnectionMonitor-Cmdlet wird der angegebene Verbindungsmonitor gestartet.</span><span class="sxs-lookup"><span data-stu-id="a3a3f-111">The Start-AzureRmNetworkWatcherConnectionMonitor cmdlet starts the specified connection monitor.</span></span>

## <span data-ttu-id="a3a3f-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a3a3f-112">EXAMPLES</span></span>

### <span data-ttu-id="a3a3f-113">Beispiel 1: Starten eines Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="a3a3f-113">Example 1: Start a connection monitor</span></span>
```
PS C:\> Start-AzureRmNetworkWatcherConnectionMonitor -NetworkWatcherName NetworkWatcher_centraluseuap -ResourceGroupName NetworkWatcherRG -Name cm
```

<span data-ttu-id="a3a3f-114">In diesem Beispiel wird der vom Namen und Netzwerkmonitor angegebene Verbindungsmonitor gestartet.</span><span class="sxs-lookup"><span data-stu-id="a3a3f-114">In this example we start connection monitor specified by name and network watcher</span></span>

## <span data-ttu-id="a3a3f-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3a3f-115">PARAMETERS</span></span>

### <span data-ttu-id="a3a3f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3a3f-116">-AsJob</span></span>
<span data-ttu-id="a3a3f-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a3a3f-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a3a3f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3a3f-118">-DefaultProfile</span></span>
<span data-ttu-id="a3a3f-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a3a3f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3a3f-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a3a3f-120">-InputObject</span></span>
<span data-ttu-id="a3a3f-121">Connection Monitor-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a3a3f-121">Connection monitor object.</span></span>

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

### <span data-ttu-id="a3a3f-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="a3a3f-122">-Location</span></span>
<span data-ttu-id="a3a3f-123">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="a3a3f-123">Location of the network watcher.</span></span>

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

### <span data-ttu-id="a3a3f-124">-Name</span><span class="sxs-lookup"><span data-stu-id="a3a3f-124">-Name</span></span>
<span data-ttu-id="a3a3f-125">Name des Verbindungs Monitors</span><span class="sxs-lookup"><span data-stu-id="a3a3f-125">The connection monitor name.</span></span>

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

### <span data-ttu-id="a3a3f-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a3a3f-126">-NetworkWatcher</span></span>
<span data-ttu-id="a3a3f-127">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="a3a3f-127">The network watcher resource.</span></span>

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

### <span data-ttu-id="a3a3f-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a3a3f-128">-NetworkWatcherName</span></span>
<span data-ttu-id="a3a3f-129">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="a3a3f-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="a3a3f-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3a3f-130">-PassThru</span></span>
<span data-ttu-id="a3a3f-131">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="a3a3f-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a3a3f-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3a3f-132">-ResourceGroupName</span></span>
<span data-ttu-id="a3a3f-133">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="a3a3f-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="a3a3f-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a3a3f-134">-ResourceId</span></span>
<span data-ttu-id="a3a3f-135">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="a3a3f-135">Resource ID.</span></span>

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

### <span data-ttu-id="a3a3f-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a3a3f-136">-Confirm</span></span>
<span data-ttu-id="a3a3f-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a3a3f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3a3f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3a3f-138">-WhatIf</span></span>
<span data-ttu-id="a3a3f-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a3a3f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3a3f-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a3a3f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3a3f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3a3f-141">CommonParameters</span></span>
<span data-ttu-id="a3a3f-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3a3f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3a3f-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3a3f-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3a3f-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a3a3f-144">INPUTS</span></span>

### <span data-ttu-id="a3a3f-145">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a3a3f-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="a3a3f-146">Parameter: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a3a3f-146">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="a3a3f-147">System. String</span><span class="sxs-lookup"><span data-stu-id="a3a3f-147">System.String</span></span>

### <span data-ttu-id="a3a3f-148">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorResult</span><span class="sxs-lookup"><span data-stu-id="a3a3f-148">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResult</span></span>
<span data-ttu-id="a3a3f-149">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a3a3f-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="a3a3f-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a3a3f-150">OUTPUTS</span></span>

### <span data-ttu-id="a3a3f-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a3a3f-151">System.Boolean</span></span>

## <span data-ttu-id="a3a3f-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="a3a3f-152">NOTES</span></span>
<span data-ttu-id="a3a3f-153">Schlüsselwörter: Azure, azurerm, arm, Ressource, Konnektivität, Verwaltung, Manager, Netzwerk, Netzwerke, Netzwerkmonitor, Verbindungsmonitor</span><span class="sxs-lookup"><span data-stu-id="a3a3f-153">Keywords: azure, azurerm, arm, resource, connectivity, management, manager, network, networking, network watcher, connection monitor</span></span>

## <span data-ttu-id="a3a3f-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a3a3f-154">RELATED LINKS</span></span>

[<span data-ttu-id="a3a3f-155">Neu – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a3a3f-155">New-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="a3a3f-156">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a3a3f-156">Get-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="a3a3f-157">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a3a3f-157">Remove-AzureRmNetworkWatcher</span></span>]()

[<span data-ttu-id="a3a3f-158">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a3a3f-158">Get-AzureRmNetworkWatcherNextHop</span></span>]()

[<span data-ttu-id="a3a3f-159">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a3a3f-159">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>]()

[<span data-ttu-id="a3a3f-160">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="a3a3f-160">Get-AzureRmNetworkWatcherTopology</span></span>]()

[<span data-ttu-id="a3a3f-161">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="a3a3f-161">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>]()

[<span data-ttu-id="a3a3f-162">Neu – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a3a3f-162">New-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="a3a3f-163">Neu – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a3a3f-163">New-AzureRmPacketCaptureFilterConfig</span></span>]()

[<span data-ttu-id="a3a3f-164">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a3a3f-164">Get-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="a3a3f-165">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a3a3f-165">Remove-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="a3a3f-166">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a3a3f-166">Stop-AzureRmNetworkWatcherPacketCapture</span></span>]()

[<span data-ttu-id="a3a3f-167">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a3a3f-167">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="a3a3f-168">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="a3a3f-168">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>]()

[<span data-ttu-id="a3a3f-169">Remove-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a3a3f-169">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="a3a3f-170">Satz-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a3a3f-170">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="a3a3f-171">Stopp-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a3a3f-171">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="a3a3f-172">Neu – AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a3a3f-172">New-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="a3a3f-173">Neu – AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3a3f-173">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>]()

[<span data-ttu-id="a3a3f-174">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a3a3f-174">Test-AzureRmNetworkWatcherIPFlow</span></span>]()

[<span data-ttu-id="a3a3f-175">Test-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="a3a3f-175">Test-AzureRmNetworkWatcherConnectivity</span></span>]()

[<span data-ttu-id="a3a3f-176">Anfang-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="a3a3f-176">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>]()

[<span data-ttu-id="a3a3f-177">Anfang-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a3a3f-177">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>]()

[<span data-ttu-id="a3a3f-178">Satz-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="a3a3f-178">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>]()

[<span data-ttu-id="a3a3f-179">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="a3a3f-179">Get-AzureRMNetworkWatcherReachabilityReport</span></span>]()

[<span data-ttu-id="a3a3f-180">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="a3a3f-180">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>]()

[<span data-ttu-id="a3a3f-181">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="a3a3f-181">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>]()
