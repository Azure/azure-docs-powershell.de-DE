---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: 093a847154c75ee7c640bda522ebf16baa04560a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665191"
---
# <span data-ttu-id="0f983-101">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="0f983-101">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="0f983-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0f983-102">SYNOPSIS</span></span>
<span data-ttu-id="0f983-103">Listet alle verfügbaren Internetdienstanbieter für einen angegebenen Azure-Bereich auf.</span><span class="sxs-lookup"><span data-stu-id="0f983-103">Lists all available internet service providers for a specified Azure region.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f983-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f983-104">SYNTAX</span></span>

### <span data-ttu-id="0f983-105">SetByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="0f983-105">SetByName (Default)</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f983-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="0f983-106">SetByResource</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f983-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="0f983-107">SetByResourceId</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -ResourceId <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f983-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0f983-108">DESCRIPTION</span></span>
<span data-ttu-id="0f983-109">Im Get-AzureRmNetworkWatcherReachabilityProvidersList werden alle verfügbaren Internetdienstanbieter für einen angegebenen Azure-Bereich aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="0f983-109">The Get-AzureRmNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="0f983-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0f983-110">EXAMPLES</span></span>

### <span data-ttu-id="0f983-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0f983-111">Example 1</span></span>
```
PS C:\> $nw = Get-AzureRmNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
PS C:\> Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcher $nw -Location "West US" -Country "United States" -State "washington" -City "seattle"

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

<span data-ttu-id="0f983-112">Listet alle verfügbaren Anbieter in Seattle auf, WA für Azure Data Center in West USA.</span><span class="sxs-lookup"><span data-stu-id="0f983-112">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

## <span data-ttu-id="0f983-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f983-113">PARAMETERS</span></span>

### <span data-ttu-id="0f983-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f983-114">-AsJob</span></span>
<span data-ttu-id="0f983-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0f983-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0f983-116">-Ort</span><span class="sxs-lookup"><span data-stu-id="0f983-116">-City</span></span>
<span data-ttu-id="0f983-117">Der Name des Orts.</span><span class="sxs-lookup"><span data-stu-id="0f983-117">The name of the city.</span></span>

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

### <span data-ttu-id="0f983-118">-Land</span><span class="sxs-lookup"><span data-stu-id="0f983-118">-Country</span></span>
<span data-ttu-id="0f983-119">Der Name des Landes.</span><span class="sxs-lookup"><span data-stu-id="0f983-119">The name of the country.</span></span>

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

### <span data-ttu-id="0f983-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f983-120">-DefaultProfile</span></span>
<span data-ttu-id="0f983-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0f983-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f983-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="0f983-122">-Location</span></span>
<span data-ttu-id="0f983-123">Optionale Azure-Bereiche zum Bereich der Abfrage.</span><span class="sxs-lookup"><span data-stu-id="0f983-123">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="0f983-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0f983-124">-NetworkWatcher</span></span>
<span data-ttu-id="0f983-125">Die Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="0f983-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="0f983-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="0f983-126">-NetworkWatcherName</span></span>
<span data-ttu-id="0f983-127">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="0f983-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="0f983-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f983-128">-ResourceGroupName</span></span>
<span data-ttu-id="0f983-129">Der Name der Netzwerk Überwachungsressourcen Gruppe.</span><span class="sxs-lookup"><span data-stu-id="0f983-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="0f983-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="0f983-130">-ResourceId</span></span>
<span data-ttu-id="0f983-131">Die ID der Netzwerk Überwachungsressource.</span><span class="sxs-lookup"><span data-stu-id="0f983-131">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="0f983-132">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="0f983-132">-State</span></span>
<span data-ttu-id="0f983-133">Der Name des Zustands.</span><span class="sxs-lookup"><span data-stu-id="0f983-133">The name of the state.</span></span>

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

### <span data-ttu-id="0f983-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f983-134">CommonParameters</span></span>
<span data-ttu-id="0f983-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f983-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f983-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f983-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f983-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0f983-137">INPUTS</span></span>

### <span data-ttu-id="0f983-138">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0f983-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="0f983-139">System. String System. Collections. Generic. List ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="0f983-139">System.String System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="0f983-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0f983-140">OUTPUTS</span></span>

### <span data-ttu-id="0f983-141">Microsoft. Azure. Commands. Network. Models. PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="0f983-141">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="0f983-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="0f983-142">NOTES</span></span>
<span data-ttu-id="0f983-143">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerk, Netzwerk-Watcher, weiter, Hop</span><span class="sxs-lookup"><span data-stu-id="0f983-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="0f983-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0f983-144">RELATED LINKS</span></span>

[<span data-ttu-id="0f983-145">Neu – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0f983-145">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="0f983-146">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0f983-146">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="0f983-147">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0f983-147">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="0f983-148">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="0f983-148">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="0f983-149">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="0f983-149">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="0f983-150">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="0f983-150">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="0f983-151">Anfang-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="0f983-151">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="0f983-152">Neu – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0f983-152">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0f983-153">Neu – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="0f983-153">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="0f983-154">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0f983-154">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0f983-155">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0f983-155">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0f983-156">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0f983-156">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)
