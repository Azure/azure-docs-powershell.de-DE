---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcher.md
ms.openlocfilehash: d312eaa9f75fc13ecba0b00aa0fea64b5d3ea2e2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841592"
---
# <span data-ttu-id="fb281-101">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fb281-101">Get-AzNetworkWatcher</span></span>

## <span data-ttu-id="fb281-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fb281-102">SYNOPSIS</span></span>
<span data-ttu-id="fb281-103">Ruft die Eigenschaften eines Netzwerkmonitors ab.</span><span class="sxs-lookup"><span data-stu-id="fb281-103">Gets the properties of a Network Watcher</span></span>

## <span data-ttu-id="fb281-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb281-104">SYNTAX</span></span>

### <span data-ttu-id="fb281-105">Erhalten</span><span class="sxs-lookup"><span data-stu-id="fb281-105">Get</span></span>
```
Get-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fb281-106">Liste</span><span class="sxs-lookup"><span data-stu-id="fb281-106">List</span></span>
```
Get-AzNetworkWatcher [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fb281-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fb281-107">DESCRIPTION</span></span>
<span data-ttu-id="fb281-108">Das Get-AzNetworkWatcher-Cmdlet ruft mindestens eine Azure Network Watcher-Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="fb281-108">The Get-AzNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="fb281-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fb281-109">EXAMPLES</span></span>

### <span data-ttu-id="fb281-110">--------------------------Beispiel 1: Abrufen eines Netzwerkmonitors--------------------------</span><span class="sxs-lookup"><span data-stu-id="fb281-110">--------------------------  Example 1: Get a Network Watcher  --------------------------</span></span>
```
Get-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="fb281-111">Ruft den Netzwerkmonitor mit dem Namen NetworkWatcher_westcentralus in der Ressourcengruppe NetworkWatcherRG ab.</span><span class="sxs-lookup"><span data-stu-id="fb281-111">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

## <span data-ttu-id="fb281-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb281-112">PARAMETERS</span></span>

### <span data-ttu-id="fb281-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb281-113">-DefaultProfile</span></span>
<span data-ttu-id="fb281-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fb281-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb281-115">-Name</span><span class="sxs-lookup"><span data-stu-id="fb281-115">-Name</span></span>
<span data-ttu-id="fb281-116">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="fb281-116">The network watcher name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb281-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb281-117">-ResourceGroupName</span></span>
<span data-ttu-id="fb281-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fb281-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb281-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb281-119">CommonParameters</span></span>
<span data-ttu-id="fb281-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb281-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb281-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb281-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb281-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fb281-122">INPUTS</span></span>

### <span data-ttu-id="fb281-123">Keine</span><span class="sxs-lookup"><span data-stu-id="fb281-123">None</span></span>

## <span data-ttu-id="fb281-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fb281-124">OUTPUTS</span></span>

### <span data-ttu-id="fb281-125">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fb281-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="fb281-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="fb281-126">NOTES</span></span>
<span data-ttu-id="fb281-127">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke, Netzwerkmonitor</span><span class="sxs-lookup"><span data-stu-id="fb281-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span> 

## <span data-ttu-id="fb281-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fb281-128">RELATED LINKS</span></span>

[<span data-ttu-id="fb281-129">Neu – AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fb281-129">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="fb281-130">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fb281-130">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="fb281-131">Neu – AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fb281-131">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fb281-132">Neu – AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="fb281-132">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="fb281-133">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fb281-133">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fb281-134">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fb281-134">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fb281-135">Stopp-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fb281-135">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fb281-136">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="fb281-136">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="fb281-137">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="fb281-137">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="fb281-138">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="fb281-138">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="fb281-139">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="fb281-139">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="fb281-140">Anfang-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="fb281-140">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
