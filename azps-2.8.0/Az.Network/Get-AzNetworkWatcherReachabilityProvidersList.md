---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: 227bd70bd67ff29015223becc6788f5043ae4776
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411040"
---
# <span data-ttu-id="2fe07-101">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="2fe07-101">Get-AzNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="2fe07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fe07-102">SYNOPSIS</span></span>
<span data-ttu-id="2fe07-103">Hier werden alle verfügbaren Internetdienstanbieter für eine bestimmte Region von Azure aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="2fe07-103">Lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="2fe07-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2fe07-104">SYNTAX</span></span>

### <span data-ttu-id="2fe07-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="2fe07-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <String[]>] [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2fe07-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2fe07-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2fe07-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="2fe07-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherLocation <String> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2fe07-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2fe07-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -ResourceId <String> [-Location <String[]>] [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2fe07-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2fe07-109">DESCRIPTION</span></span>
<span data-ttu-id="2fe07-110">Im Get-AzNetworkWatcherReachabilityProvidersList werden alle verfügbaren Internetdienstanbieter für eine bestimmte Region von Azure aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="2fe07-110">The Get-AzNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="2fe07-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2fe07-111">EXAMPLES</span></span>

### <span data-ttu-id="2fe07-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2fe07-112">Example 1</span></span>
```
PS C:\> $nw = Get-AzNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
PS C:\> Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher $nw -Location "West US" -Country "United States" -State "washington" -City "seattle"

"countries" : [
    {
        "countryName" : "United States",
        "states" : [
            {
                "stateName" : "washington",
                "cities" : [
                    {
                        "cityName" : "seattle",
                        "providers" : [
                            "Comcast Cable Communications, Inc. - ASN 7922",
                            "Comcast Cable Communications, LLC - ASN 7922",
                            "Level 3 Communications, Inc. (GBLX) - ASN 3549",
                            "Qwest Communications Company, LLC - ASN 209"
                        ]
                    }
                ]
            }
        ]
    }
]
```

<span data-ttu-id="2fe07-113">Listet alle verfügbaren Anbieter in Seattle, WASHINGTON für Azure Data Center im Westen der USA auf.</span><span class="sxs-lookup"><span data-stu-id="2fe07-113">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

## <span data-ttu-id="2fe07-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2fe07-114">PARAMETERS</span></span>

### <span data-ttu-id="2fe07-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2fe07-115">-AsJob</span></span>
<span data-ttu-id="2fe07-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2fe07-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2fe07-117">-Ort</span><span class="sxs-lookup"><span data-stu-id="2fe07-117">-City</span></span>
<span data-ttu-id="2fe07-118">Der Name der Stadt.</span><span class="sxs-lookup"><span data-stu-id="2fe07-118">The name of the city.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe07-119">-Country</span><span class="sxs-lookup"><span data-stu-id="2fe07-119">-Country</span></span>
<span data-ttu-id="2fe07-120">Der Name des Landes.</span><span class="sxs-lookup"><span data-stu-id="2fe07-120">The name of the country.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe07-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fe07-121">-DefaultProfile</span></span>
<span data-ttu-id="2fe07-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2fe07-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fe07-123">-Location</span><span class="sxs-lookup"><span data-stu-id="2fe07-123">-Location</span></span>
<span data-ttu-id="2fe07-124">Optionale Azure-Regionen, auf die der Abfragebereich begrenzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2fe07-124">Optional Azure regions to scope the query to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe07-125">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2fe07-125">-NetworkWatcher</span></span>
<span data-ttu-id="2fe07-126">Die Netzwerk-Watcher-Ressource.</span><span class="sxs-lookup"><span data-stu-id="2fe07-126">The network watcher resource.</span></span>

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

### <span data-ttu-id="2fe07-127">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="2fe07-127">-NetworkWatcherLocation</span></span>
<span data-ttu-id="2fe07-128">Speicherort der Netzwerk-Watcher.</span><span class="sxs-lookup"><span data-stu-id="2fe07-128">Location of the network watcher.</span></span>

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

### <span data-ttu-id="2fe07-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="2fe07-129">-NetworkWatcherName</span></span>
<span data-ttu-id="2fe07-130">Der Name der Netzwerk-Watcher.</span><span class="sxs-lookup"><span data-stu-id="2fe07-130">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: ResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe07-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fe07-131">-ResourceGroupName</span></span>
<span data-ttu-id="2fe07-132">Der Name der Ressourcengruppe "Netzwerk-Watcher".</span><span class="sxs-lookup"><span data-stu-id="2fe07-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="2fe07-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2fe07-133">-ResourceId</span></span>
<span data-ttu-id="2fe07-134">Die ID der Netzwerk-Watcher-Ressource.</span><span class="sxs-lookup"><span data-stu-id="2fe07-134">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="2fe07-135">-State</span><span class="sxs-lookup"><span data-stu-id="2fe07-135">-State</span></span>
<span data-ttu-id="2fe07-136">Der Name des Zustands.</span><span class="sxs-lookup"><span data-stu-id="2fe07-136">The name of the state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fe07-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fe07-137">CommonParameters</span></span>
<span data-ttu-id="2fe07-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fe07-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fe07-139">Weitere Informationen finden Sie unter [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2fe07-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fe07-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2fe07-140">INPUTS</span></span>

### <span data-ttu-id="2fe07-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2fe07-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="2fe07-142">System.String</span><span class="sxs-lookup"><span data-stu-id="2fe07-142">System.String</span></span>

## <span data-ttu-id="2fe07-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2fe07-143">OUTPUTS</span></span>

### <span data-ttu-id="2fe07-144">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="2fe07-144">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="2fe07-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2fe07-145">NOTES</span></span>
<span data-ttu-id="2fe07-146">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span><span class="sxs-lookup"><span data-stu-id="2fe07-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="2fe07-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2fe07-147">RELATED LINKS</span></span>

[<span data-ttu-id="2fe07-148">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2fe07-148">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="2fe07-149">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2fe07-149">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="2fe07-150">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2fe07-150">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="2fe07-151">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2fe07-151">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="2fe07-152">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2fe07-152">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="2fe07-153">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2fe07-153">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="2fe07-154">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2fe07-154">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="2fe07-155">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2fe07-155">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2fe07-156">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2fe07-156">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="2fe07-157">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2fe07-157">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2fe07-158">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2fe07-158">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2fe07-159">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2fe07-159">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2fe07-160">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="2fe07-160">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="2fe07-161">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2fe07-161">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="2fe07-162">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="2fe07-162">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="2fe07-163">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2fe07-163">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2fe07-164">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2fe07-164">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2fe07-165">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2fe07-165">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2fe07-166">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="2fe07-166">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="2fe07-167">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2fe07-167">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2fe07-168">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2fe07-168">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2fe07-169">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="2fe07-169">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="2fe07-170">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="2fe07-170">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="2fe07-171">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="2fe07-171">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="2fe07-172">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="2fe07-172">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="2fe07-173">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="2fe07-173">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="2fe07-174">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2fe07-174">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
