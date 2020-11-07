---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherreachabilityreport
schema: 2.0.0
ms.openlocfilehash: 75335fb09bb8f4187879ab69ab138952cc873993
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850768"
---
# <span data-ttu-id="783d0-101">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="783d0-101">Get-AzureRMNetworkWatcherReachabilityReport</span></span>

## <span data-ttu-id="783d0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="783d0-102">SYNOPSIS</span></span>
<span data-ttu-id="783d0-103">Ruft den relativen Latenz Faktor für Internetdienstanbieter von einem angegebenen Speicherort zu Azure-Regionen ab.</span><span class="sxs-lookup"><span data-stu-id="783d0-103">Gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="783d0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="783d0-104">SYNTAX</span></span>

### <span data-ttu-id="783d0-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="783d0-105">SetByName (Default)</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="783d0-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="783d0-106">SetByResource</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="783d0-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="783d0-107">SetByResourceId</span></span>
```
Get-AzureRMNetworkWatcherReachabilityReport -ResourceId <String>
 [-Provider <System.Collections.Generic.List`1[System.String]>]
 [-Location <System.Collections.Generic.List`1[System.String]>] -StartTime <DateTime> -EndTime <DateTime>
 [-Country <String>] [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="783d0-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="783d0-108">DESCRIPTION</span></span>
<span data-ttu-id="783d0-109">Der Get-AzureRmNetworkWatcherReachabilityReport ruft den relativen Latenz Faktor für Internetdienstanbieter von einem angegebenen Speicherort zu Azure-Regionen ab.</span><span class="sxs-lookup"><span data-stu-id="783d0-109">The Get-AzureRmNetworkWatcherReachabilityReport gets the relative latency score for internet service providers from a specified location to Azure regions.</span></span>

## <span data-ttu-id="783d0-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="783d0-110">EXAMPLES</span></span>

### <span data-ttu-id="783d0-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="783d0-111">Example 1</span></span>
```
$nw = Get-AzureRmNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
Get-AzureRmNetworkWatcherReachabilityReport -NetworkWatcher $nw -Location "West US" -Country "United States" -StartTime "2017-10-10" -EndTime "2017-10-12"

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

<span data-ttu-id="783d0-112">Ruft relative Latenzen für das Azure-Rechenzentrum in West-US von 2017-10-10 bis 2017-10-12 innerhalb des United-Bundesstaates ab.</span><span class="sxs-lookup"><span data-stu-id="783d0-112">Gets relative latencies to Azure Data Center in West US from 2017-10-10 to 2017-10-12 inside United State.</span></span>

## <span data-ttu-id="783d0-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="783d0-113">PARAMETERS</span></span>

### <span data-ttu-id="783d0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="783d0-114">-AsJob</span></span>
<span data-ttu-id="783d0-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="783d0-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="783d0-116">-Ort</span><span class="sxs-lookup"><span data-stu-id="783d0-116">-City</span></span>
<span data-ttu-id="783d0-117">Der Name des Orts.</span><span class="sxs-lookup"><span data-stu-id="783d0-117">The name of the city.</span></span>

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

### <span data-ttu-id="783d0-118">-Land</span><span class="sxs-lookup"><span data-stu-id="783d0-118">-Country</span></span>
<span data-ttu-id="783d0-119">Der Name des Landes.</span><span class="sxs-lookup"><span data-stu-id="783d0-119">The name of the country.</span></span>

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

### <span data-ttu-id="783d0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="783d0-120">-DefaultProfile</span></span>
<span data-ttu-id="783d0-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="783d0-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="783d0-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="783d0-122">-EndTime</span></span>
<span data-ttu-id="783d0-123">Die Endzeit für den Azure-Erreichbarkeits Bericht.</span><span class="sxs-lookup"><span data-stu-id="783d0-123">The end time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="783d0-124">-Standort</span><span class="sxs-lookup"><span data-stu-id="783d0-124">-Location</span></span>
<span data-ttu-id="783d0-125">Optionale Azure-Bereiche zum Bereich der Abfrage.</span><span class="sxs-lookup"><span data-stu-id="783d0-125">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="783d0-126">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="783d0-126">-NetworkWatcher</span></span>
<span data-ttu-id="783d0-127">Die Netzwerk Überwachungsressource</span><span class="sxs-lookup"><span data-stu-id="783d0-127">The network watcher resource</span></span>

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

### <span data-ttu-id="783d0-128">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="783d0-128">-NetworkWatcherName</span></span>
<span data-ttu-id="783d0-129">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="783d0-129">The name of network watcher.</span></span>

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

### <span data-ttu-id="783d0-130">-Anbieter</span><span class="sxs-lookup"><span data-stu-id="783d0-130">-Provider</span></span>
<span data-ttu-id="783d0-131">Liste der Internet Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="783d0-131">List of Internet service providers.</span></span>

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

### <span data-ttu-id="783d0-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="783d0-132">-ResourceGroupName</span></span>
<span data-ttu-id="783d0-133">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="783d0-133">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="783d0-134">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="783d0-134">-ResourceId</span></span>
<span data-ttu-id="783d0-135">Die ID der Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="783d0-135">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="783d0-136">-Startzeit</span><span class="sxs-lookup"><span data-stu-id="783d0-136">-StartTime</span></span>
<span data-ttu-id="783d0-137">Die Startzeit für den Azure-Erreichbarkeits Bericht.</span><span class="sxs-lookup"><span data-stu-id="783d0-137">The start time for the Azure reachability report.</span></span>

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

### <span data-ttu-id="783d0-138">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="783d0-138">-State</span></span>
<span data-ttu-id="783d0-139">Der Name des Zustands.</span><span class="sxs-lookup"><span data-stu-id="783d0-139">The name of the state.</span></span>

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

### <span data-ttu-id="783d0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="783d0-140">CommonParameters</span></span>
<span data-ttu-id="783d0-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="783d0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="783d0-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="783d0-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="783d0-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="783d0-143">INPUTS</span></span>

### <span data-ttu-id="783d0-144">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="783d0-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="783d0-145">System. String</span><span class="sxs-lookup"><span data-stu-id="783d0-145">System.String</span></span>

## <span data-ttu-id="783d0-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="783d0-146">OUTPUTS</span></span>

### <span data-ttu-id="783d0-147">Microsoft. Azure. Commands. Network. Models. PSAzureReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="783d0-147">Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport</span></span>

## <span data-ttu-id="783d0-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="783d0-148">NOTES</span></span>
<span data-ttu-id="783d0-149">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerkmonitor, Erreichbarkeit, Bericht</span><span class="sxs-lookup"><span data-stu-id="783d0-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, reachability, report</span></span>

## <span data-ttu-id="783d0-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="783d0-150">RELATED LINKS</span></span>

[<span data-ttu-id="783d0-151">Neu – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="783d0-151">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="783d0-152">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="783d0-152">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="783d0-153">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="783d0-153">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="783d0-154">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="783d0-154">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="783d0-155">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="783d0-155">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="783d0-156">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="783d0-156">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="783d0-157">Anfang-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="783d0-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="783d0-158">Neu – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="783d0-158">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="783d0-159">Neu – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="783d0-159">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="783d0-160">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="783d0-160">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="783d0-161">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="783d0-161">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="783d0-162">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="783d0-162">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)
