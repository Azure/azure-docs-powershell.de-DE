---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: 6da0a36ee5e394008ea1d1de4a16f7982227ca06
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841560"
---
# <span data-ttu-id="8b97b-101">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="8b97b-101">Get-AzNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="8b97b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8b97b-102">SYNOPSIS</span></span>
<span data-ttu-id="8b97b-103">Ruft den relativen Latenz Faktor für Internetdienstanbieter von einem angegebenen Speicherort zu Azure-Regionen ab.</span><span class="sxs-lookup"><span data-stu-id="8b97b-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="8b97b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b97b-104">SYNTAX</span></span>

### <span data-ttu-id="8b97b-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="8b97b-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8b97b-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="8b97b-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8b97b-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="8b97b-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8b97b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b97b-108">DESCRIPTION</span></span>
<span data-ttu-id="8b97b-109">Der Get-AzNetworkWatcherReachabilityReport ruft den relativen Latenz Faktor für Internetdienstanbieter von einem angegebenen Speicherort zu Azure-Regionen ab.</span><span class="sxs-lookup"><span data-stu-id="8b97b-109">The Get-AzNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="8b97b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8b97b-110">EXAMPLES</span></span>

### <span data-ttu-id="8b97b-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8b97b-111">Example 1</span></span>
```
$nw = Get-AzNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher $nw -Location "West US" -Country "United States" -StartTime "2017-10-10" -EndTime "2017-10-12"

"aggregationLevel" : "Country",
"providerLocation" : {
    "country" : "United States"
},
"reachabilityReport" : [
    {
        "provider" : "Frontier Communications of America, Inc. - ASN 5650",
        "azureLocation": "West US",
        "latencies": [
            {
                "timeStamp": "2017-10-10T00:00:00Z",
                "score": 94
            },
            {
                "timeStamp": "2017-10-11T00:00:00Z",
                "score": 94
            },
            {
                "timeStamp": "2017-10-12T00:00:00Z",
                "score": 94    
            }
        ]  
    }
]
```

<span data-ttu-id="8b97b-112">Ruft relative Latenzen für das Azure-Rechenzentrum in West-US von 2017-10-10 bis 2017-10-12 innerhalb des United-Bundesstaates ab.</span><span class="sxs-lookup"><span data-stu-id="8b97b-112">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="8b97b-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b97b-113">PARAMETERS</span></span>

### <span data-ttu-id="8b97b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b97b-114">-AsJob</span></span>
<span data-ttu-id="8b97b-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8b97b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8b97b-116">-Ort</span><span class="sxs-lookup"><span data-stu-id="8b97b-116">-City</span></span>
<span data-ttu-id="8b97b-117">Der Name des Orts.</span><span class="sxs-lookup"><span data-stu-id="8b97b-117">The name of the city.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b97b-118">-Land</span><span class="sxs-lookup"><span data-stu-id="8b97b-118">-Country</span></span>
<span data-ttu-id="8b97b-119">Der Name des Landes.</span><span class="sxs-lookup"><span data-stu-id="8b97b-119">The name of the country.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b97b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b97b-120">-DefaultProfile</span></span>
<span data-ttu-id="8b97b-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8b97b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b97b-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="8b97b-122">-EndTime</span></span>
<span data-ttu-id="8b97b-123">Die Endzeit für den Azure-Erreichbarkeits Bericht.</span><span class="sxs-lookup"><span data-stu-id="8b97b-123">The end time for the Azure reachability report.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b97b-124">-Standort</span><span class="sxs-lookup"><span data-stu-id="8b97b-124">-Location</span></span>
<span data-ttu-id="8b97b-125">Optionale Azure-Bereiche zum Bereich der Abfrage.</span><span class="sxs-lookup"><span data-stu-id="8b97b-125">Optional Azure regions to scope the query to.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b97b-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8b97b-126">-NetworkWatcher</span></span>
<span data-ttu-id="8b97b-127">Die Netzwerk Überwachungsressource</span><span class="sxs-lookup"><span data-stu-id="8b97b-127">The network watcher resource</span></span>

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

### <span data-ttu-id="8b97b-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="8b97b-128">-NetworkWatcherName</span></span>
<span data-ttu-id="8b97b-129">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="8b97b-129">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: ResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b97b-130">-Anbieter</span><span class="sxs-lookup"><span data-stu-id="8b97b-130">-Provider</span></span>
<span data-ttu-id="8b97b-131">Liste der Internet Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="8b97b-131">List of Internet service providers.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b97b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b97b-132">-ResourceGroupName</span></span>
<span data-ttu-id="8b97b-133">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="8b97b-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="8b97b-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="8b97b-134">-ResourceId</span></span>
<span data-ttu-id="8b97b-135">Die ID der Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="8b97b-135">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="8b97b-136">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="8b97b-136">-StartTime</span></span>
<span data-ttu-id="8b97b-137">Die Startzeit für den Azure-Erreichbarkeits Bericht.</span><span class="sxs-lookup"><span data-stu-id="8b97b-137">The start time for the Azure reachability report.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b97b-138">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="8b97b-138">-State</span></span>
<span data-ttu-id="8b97b-139">Der Name des Zustands.</span><span class="sxs-lookup"><span data-stu-id="8b97b-139">The name of the state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b97b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b97b-140">CommonParameters</span></span>
<span data-ttu-id="8b97b-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b97b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b97b-142">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b97b-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b97b-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8b97b-143">INPUTS</span></span>

### <span data-ttu-id="8b97b-144">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8b97b-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="8b97b-145">System. String</span><span class="sxs-lookup"><span data-stu-id="8b97b-145">System.String</span></span>

## <span data-ttu-id="8b97b-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8b97b-146">OUTPUTS</span></span>

### <span data-ttu-id="8b97b-147">Microsoft. Azure. Commands. Network. Models. PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="8b97b-147">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="8b97b-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="8b97b-148">NOTES</span></span>
<span data-ttu-id="8b97b-149">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerkmonitor, Erreichbarkeit, Bericht</span><span class="sxs-lookup"><span data-stu-id="8b97b-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="8b97b-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8b97b-150">RELATED LINKS</span></span>

[<span data-ttu-id="8b97b-151">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8b97b-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="8b97b-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8b97b-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="8b97b-153">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="8b97b-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="8b97b-154">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="8b97b-154">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="8b97b-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="8b97b-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="8b97b-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="8b97b-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="8b97b-157">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="8b97b-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="8b97b-158">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8b97b-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8b97b-159">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="8b97b-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="8b97b-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8b97b-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8b97b-161">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8b97b-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="8b97b-162">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8b97b-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)
