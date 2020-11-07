---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: 805c8d31b075a39fa8ccc407024aa5a32a91fdb6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841564"
---
# <span data-ttu-id="56f85-101">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="56f85-101">Get-AzNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="56f85-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="56f85-102">SYNOPSIS</span></span>
<span data-ttu-id="56f85-103">Listet alle verfügbaren Internetdienstanbieter für einen angegebenen Azure-Bereich auf.</span><span class="sxs-lookup"><span data-stu-id="56f85-103">Lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="56f85-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="56f85-104">SYNTAX</span></span>

### <span data-ttu-id="56f85-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="56f85-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56f85-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="56f85-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56f85-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="56f85-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -ResourceId <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56f85-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="56f85-108">DESCRIPTION</span></span>
<span data-ttu-id="56f85-109">Im Get-AzNetworkWatcherReachabilityProvidersList werden alle verfügbaren Internetdienstanbieter für einen angegebenen Azure-Bereich aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="56f85-109">The Get-AzNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="56f85-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="56f85-110">EXAMPLES</span></span>

### <span data-ttu-id="56f85-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="56f85-111">Example 1</span></span>
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

<span data-ttu-id="56f85-112">Listet alle verfügbaren Anbieter in Seattle auf, WA für Azure Data Center in West USA.</span><span class="sxs-lookup"><span data-stu-id="56f85-112">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

## <span data-ttu-id="56f85-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="56f85-113">PARAMETERS</span></span>

### <span data-ttu-id="56f85-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="56f85-114">-AsJob</span></span>
<span data-ttu-id="56f85-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="56f85-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="56f85-116">-Ort</span><span class="sxs-lookup"><span data-stu-id="56f85-116">-City</span></span>
<span data-ttu-id="56f85-117">Der Name des Orts.</span><span class="sxs-lookup"><span data-stu-id="56f85-117">The name of the city.</span></span>

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

### <span data-ttu-id="56f85-118">-Land</span><span class="sxs-lookup"><span data-stu-id="56f85-118">-Country</span></span>
<span data-ttu-id="56f85-119">Der Name des Landes.</span><span class="sxs-lookup"><span data-stu-id="56f85-119">The name of the country.</span></span>

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

### <span data-ttu-id="56f85-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56f85-120">-DefaultProfile</span></span>
<span data-ttu-id="56f85-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="56f85-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56f85-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="56f85-122">-Location</span></span>
<span data-ttu-id="56f85-123">Optionale Azure-Bereiche zum Bereich der Abfrage.</span><span class="sxs-lookup"><span data-stu-id="56f85-123">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="56f85-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="56f85-124">-NetworkWatcher</span></span>
<span data-ttu-id="56f85-125">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="56f85-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="56f85-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="56f85-126">-NetworkWatcherName</span></span>
<span data-ttu-id="56f85-127">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="56f85-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="56f85-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56f85-128">-ResourceGroupName</span></span>
<span data-ttu-id="56f85-129">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="56f85-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="56f85-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="56f85-130">-ResourceId</span></span>
<span data-ttu-id="56f85-131">Die ID der Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="56f85-131">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="56f85-132">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="56f85-132">-State</span></span>
<span data-ttu-id="56f85-133">Der Name des Zustands.</span><span class="sxs-lookup"><span data-stu-id="56f85-133">The name of the state.</span></span>

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

### <span data-ttu-id="56f85-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56f85-134">CommonParameters</span></span>
<span data-ttu-id="56f85-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56f85-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56f85-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56f85-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56f85-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="56f85-137">INPUTS</span></span>

### <span data-ttu-id="56f85-138">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="56f85-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="56f85-139">System. String System. Collections. Generic. List ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="56f85-139">System.String System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="56f85-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="56f85-140">OUTPUTS</span></span>

### <span data-ttu-id="56f85-141">Microsoft. Azure. Commands. Network. Models. PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="56f85-141">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="56f85-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="56f85-142">NOTES</span></span>
<span data-ttu-id="56f85-143">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerk-Watcher, weiter, Hop</span><span class="sxs-lookup"><span data-stu-id="56f85-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="56f85-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="56f85-144">RELATED LINKS</span></span>

[<span data-ttu-id="56f85-145">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="56f85-145">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="56f85-146">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="56f85-146">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="56f85-147">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="56f85-147">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="56f85-148">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="56f85-148">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="56f85-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="56f85-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="56f85-150">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="56f85-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="56f85-151">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="56f85-151">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="56f85-152">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="56f85-152">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="56f85-153">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="56f85-153">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="56f85-154">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="56f85-154">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="56f85-155">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="56f85-155">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="56f85-156">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="56f85-156">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)
