---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: a4e9c9a928d3a6c3ddeb7afa754cc957089a2283
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176619"
---
# <span data-ttu-id="9a68c-101">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="9a68c-101">Get-AzNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="9a68c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9a68c-102">SYNOPSIS</span></span>
<span data-ttu-id="9a68c-103">Listet alle verfügbaren Internetdienstanbieter für einen angegebenen Azure-Bereich auf.</span><span class="sxs-lookup"><span data-stu-id="9a68c-103">Lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="9a68c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a68c-104">SYNTAX</span></span>

### <span data-ttu-id="9a68c-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="9a68c-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <String[]>] [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a68c-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="9a68c-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9a68c-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="9a68c-107">SetByLocation</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherLocation <String> [-Location <String[]>]
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9a68c-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="9a68c-108">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -ResourceId <String> [-Location <String[]>] [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a68c-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9a68c-109">DESCRIPTION</span></span>
<span data-ttu-id="9a68c-110">Im Get-AzNetworkWatcherReachabilityProvidersList werden alle verfügbaren Internetdienstanbieter für einen angegebenen Azure-Bereich aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="9a68c-110">The Get-AzNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="9a68c-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9a68c-111">EXAMPLES</span></span>

### <span data-ttu-id="9a68c-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9a68c-112">Example 1</span></span>
```powershell
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

<span data-ttu-id="9a68c-113">Listet alle verfügbaren Anbieter in Seattle auf, WA für Azure Data Center in West USA.</span><span class="sxs-lookup"><span data-stu-id="9a68c-113">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

### <span data-ttu-id="9a68c-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="9a68c-114">Example 2</span></span>

<span data-ttu-id="9a68c-115">Listet alle verfügbaren Internetdienstanbieter für einen angegebenen Azure-Bereich auf.</span><span class="sxs-lookup"><span data-stu-id="9a68c-115">Lists all available internet service providers for a specified Azure region.</span></span> <span data-ttu-id="9a68c-116">automatisch</span><span class="sxs-lookup"><span data-stu-id="9a68c-116">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName nw1 -ResourceGroupName myresourcegroup
```

## <span data-ttu-id="9a68c-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a68c-117">PARAMETERS</span></span>

### <span data-ttu-id="9a68c-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a68c-118">-AsJob</span></span>
<span data-ttu-id="9a68c-119">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9a68c-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9a68c-120">-Ort</span><span class="sxs-lookup"><span data-stu-id="9a68c-120">-City</span></span>
<span data-ttu-id="9a68c-121">Der Name des Orts.</span><span class="sxs-lookup"><span data-stu-id="9a68c-121">The name of the city.</span></span>

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

### <span data-ttu-id="9a68c-122">-Land</span><span class="sxs-lookup"><span data-stu-id="9a68c-122">-Country</span></span>
<span data-ttu-id="9a68c-123">Der Name des Landes.</span><span class="sxs-lookup"><span data-stu-id="9a68c-123">The name of the country.</span></span>

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

### <span data-ttu-id="9a68c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a68c-124">-DefaultProfile</span></span>
<span data-ttu-id="9a68c-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9a68c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a68c-126">-Standort</span><span class="sxs-lookup"><span data-stu-id="9a68c-126">-Location</span></span>
<span data-ttu-id="9a68c-127">Optionale Azure-Bereiche zum Bereich der Abfrage.</span><span class="sxs-lookup"><span data-stu-id="9a68c-127">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="9a68c-128">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9a68c-128">-NetworkWatcher</span></span>
<span data-ttu-id="9a68c-129">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="9a68c-129">The network watcher resource.</span></span>

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

### <span data-ttu-id="9a68c-130">-NetworkWatcherLocation</span><span class="sxs-lookup"><span data-stu-id="9a68c-130">-NetworkWatcherLocation</span></span>
<span data-ttu-id="9a68c-131">Der Speicherort des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="9a68c-131">Location of the network watcher.</span></span>

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

### <span data-ttu-id="9a68c-132">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="9a68c-132">-NetworkWatcherName</span></span>
<span data-ttu-id="9a68c-133">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="9a68c-133">The name of network watcher.</span></span>

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

### <span data-ttu-id="9a68c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a68c-134">-ResourceGroupName</span></span>
<span data-ttu-id="9a68c-135">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="9a68c-135">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="9a68c-136">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="9a68c-136">-ResourceId</span></span>
<span data-ttu-id="9a68c-137">Die ID der Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="9a68c-137">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="9a68c-138">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="9a68c-138">-State</span></span>
<span data-ttu-id="9a68c-139">Der Name des Zustands.</span><span class="sxs-lookup"><span data-stu-id="9a68c-139">The name of the state.</span></span>

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

### <span data-ttu-id="9a68c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a68c-140">CommonParameters</span></span>
<span data-ttu-id="9a68c-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a68c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a68c-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a68c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a68c-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9a68c-143">INPUTS</span></span>

### <span data-ttu-id="9a68c-144">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9a68c-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="9a68c-145">System. String</span><span class="sxs-lookup"><span data-stu-id="9a68c-145">System.String</span></span>

## <span data-ttu-id="9a68c-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9a68c-146">OUTPUTS</span></span>

### <span data-ttu-id="9a68c-147">Microsoft. Azure. Commands. Network. Models. PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="9a68c-147">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="9a68c-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="9a68c-148">NOTES</span></span>
<span data-ttu-id="9a68c-149">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerk-Watcher, weiter, Hop</span><span class="sxs-lookup"><span data-stu-id="9a68c-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="9a68c-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9a68c-150">RELATED LINKS</span></span>

[<span data-ttu-id="9a68c-151">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9a68c-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="9a68c-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9a68c-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="9a68c-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9a68c-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="9a68c-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="9a68c-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="9a68c-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="9a68c-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="9a68c-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="9a68c-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="9a68c-157">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="9a68c-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="9a68c-158">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9a68c-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9a68c-159">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="9a68c-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="9a68c-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9a68c-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9a68c-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9a68c-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9a68c-162">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9a68c-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9a68c-163">Neu – AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="9a68c-163">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="9a68c-164">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="9a68c-164">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="9a68c-165">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="9a68c-165">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="9a68c-166">Stopp-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9a68c-166">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9a68c-167">Anfang-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9a68c-167">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9a68c-168">Satz-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9a68c-168">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9a68c-169">Satz-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="9a68c-169">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="9a68c-170">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9a68c-170">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9a68c-171">Neu – AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9a68c-171">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="9a68c-172">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="9a68c-172">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="9a68c-173">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="9a68c-173">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="9a68c-174">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="9a68c-174">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="9a68c-175">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="9a68c-175">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="9a68c-176">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="9a68c-176">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="9a68c-177">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="9a68c-177">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
