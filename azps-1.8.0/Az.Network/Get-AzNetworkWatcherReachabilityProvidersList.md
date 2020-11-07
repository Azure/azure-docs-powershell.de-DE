---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: cf35292be5005a957e245370a5b15b78bb7d4fa6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660725"
---
# <span data-ttu-id="c2166-101">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="c2166-101">Get-AzNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="c2166-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c2166-102">SYNOPSIS</span></span>
<span data-ttu-id="c2166-103">Listet alle verfügbaren Internetdienstanbieter für einen angegebenen Azure-Bereich auf.</span><span class="sxs-lookup"><span data-stu-id="c2166-103">Lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="c2166-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2166-104">SYNTAX</span></span>

### <span data-ttu-id="c2166-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c2166-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <String[]>] [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2166-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c2166-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2166-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="c2166-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherLocation <String> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2166-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c2166-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -ResourceId <String> [-Location <String[]>] [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2166-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2166-109">DESCRIPTION</span></span>
<span data-ttu-id="c2166-110">Im Get-AzNetworkWatcherReachabilityProvidersList werden alle verfügbaren Internetdienstanbieter für einen angegebenen Azure-Bereich aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c2166-110">The Get-AzNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="c2166-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c2166-111">EXAMPLES</span></span>

### <span data-ttu-id="c2166-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c2166-112">Example 1</span></span>
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

<span data-ttu-id="c2166-113">Listet alle verfügbaren Anbieter in Seattle auf, WA für Azure Data Center in West USA.</span><span class="sxs-lookup"><span data-stu-id="c2166-113">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

## <span data-ttu-id="c2166-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2166-114">PARAMETERS</span></span>

### <span data-ttu-id="c2166-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c2166-115">-AsJob</span></span>
<span data-ttu-id="c2166-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c2166-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c2166-117">-Ort</span><span class="sxs-lookup"><span data-stu-id="c2166-117">-City</span></span>
<span data-ttu-id="c2166-118">Der Name des Orts.</span><span class="sxs-lookup"><span data-stu-id="c2166-118">The name of the city.</span></span>

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

### <span data-ttu-id="c2166-119">-Land</span><span class="sxs-lookup"><span data-stu-id="c2166-119">-Country</span></span>
<span data-ttu-id="c2166-120">Der Name des Landes.</span><span class="sxs-lookup"><span data-stu-id="c2166-120">The name of the country.</span></span>

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

### <span data-ttu-id="c2166-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2166-121">-DefaultProfile</span></span>
<span data-ttu-id="c2166-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c2166-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2166-123">-Standort</span><span class="sxs-lookup"><span data-stu-id="c2166-123">-Location</span></span>
<span data-ttu-id="c2166-124">Optionale Azure-Bereiche zum Bereich der Abfrage.</span><span class="sxs-lookup"><span data-stu-id="c2166-124">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="c2166-125">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c2166-125">-NetworkWatcher</span></span>
<span data-ttu-id="c2166-126">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="c2166-126">The network watcher resource.</span></span>

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

### <span data-ttu-id="c2166-127">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="c2166-127">-NetworkWatcherLocation</span></span>
<span data-ttu-id="c2166-128">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="c2166-128">Location of the network watcher.</span></span>

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

### <span data-ttu-id="c2166-129">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="c2166-129">-NetworkWatcherName</span></span>
<span data-ttu-id="c2166-130">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="c2166-130">The name of network watcher.</span></span>

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

### <span data-ttu-id="c2166-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2166-131">-ResourceGroupName</span></span>
<span data-ttu-id="c2166-132">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="c2166-132">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="c2166-133">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c2166-133">-ResourceId</span></span>
<span data-ttu-id="c2166-134">Die ID der Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="c2166-134">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="c2166-135">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="c2166-135">-State</span></span>
<span data-ttu-id="c2166-136">Der Name des Zustands.</span><span class="sxs-lookup"><span data-stu-id="c2166-136">The name of the state.</span></span>

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

### <span data-ttu-id="c2166-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2166-137">CommonParameters</span></span>
<span data-ttu-id="c2166-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2166-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2166-139">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2166-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2166-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c2166-140">INPUTS</span></span>

### <span data-ttu-id="c2166-141">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c2166-141">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="c2166-142">System. String</span><span class="sxs-lookup"><span data-stu-id="c2166-142">System.String</span></span>

## <span data-ttu-id="c2166-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c2166-143">OUTPUTS</span></span>

### <span data-ttu-id="c2166-144">Microsoft. Azure. Commands. Network. Models. PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="c2166-144">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="c2166-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="c2166-145">NOTES</span></span>
<span data-ttu-id="c2166-146">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerk-Watcher, weiter, Hop</span><span class="sxs-lookup"><span data-stu-id="c2166-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="c2166-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c2166-147">RELATED LINKS</span></span>

[<span data-ttu-id="c2166-148">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c2166-148">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="c2166-149">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c2166-149">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="c2166-150">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c2166-150">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="c2166-151">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c2166-151">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="c2166-152">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c2166-152">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c2166-153">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c2166-153">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="c2166-154">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c2166-154">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="c2166-155">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c2166-155">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c2166-156">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c2166-156">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="c2166-157">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c2166-157">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c2166-158">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c2166-158">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c2166-159">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c2166-159">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c2166-160">Neu – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2166-160">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="c2166-161">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c2166-161">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="c2166-162">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="c2166-162">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="c2166-163">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c2166-163">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c2166-164">Anfang-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c2166-164">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c2166-165">Satz-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c2166-165">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c2166-166">Satz-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="c2166-166">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="c2166-167">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c2166-167">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c2166-168">Neu – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c2166-168">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="c2166-169">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="c2166-169">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="c2166-170">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="c2166-170">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="c2166-171">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="c2166-171">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="c2166-172">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="c2166-172">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="c2166-173">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="c2166-173">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="c2166-174">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="c2166-174">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
