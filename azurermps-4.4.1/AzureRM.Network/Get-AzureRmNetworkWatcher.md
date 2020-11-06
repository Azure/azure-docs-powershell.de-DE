---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcher.md
ms.openlocfilehash: d69c4b3a21849db14d53760c8796b91399e742b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504845"
---
# <span data-ttu-id="9d0da-101">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9d0da-101">Get-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="9d0da-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9d0da-102">SYNOPSIS</span></span>
<span data-ttu-id="9d0da-103">Ruft die Eigenschaften eines Netzwerkmonitors ab.</span><span class="sxs-lookup"><span data-stu-id="9d0da-103">Gets the properties of a Network Watcher</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d0da-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d0da-104">SYNTAX</span></span>

### <span data-ttu-id="9d0da-105">Erhalten</span><span class="sxs-lookup"><span data-stu-id="9d0da-105">Get</span></span>
```
Get-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9d0da-106">Liste</span><span class="sxs-lookup"><span data-stu-id="9d0da-106">List</span></span>
```
Get-AzureRmNetworkWatcher [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9d0da-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9d0da-107">DESCRIPTION</span></span>
<span data-ttu-id="9d0da-108">Das Get-AzureRmNetworkWatcher-Cmdlet ruft mindestens eine Azure Network Watcher-Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="9d0da-108">The Get-AzureRmNetworkWatcher cmdlet gets one or more Azure Network Watcher resources.</span></span>

## <span data-ttu-id="9d0da-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9d0da-109">EXAMPLES</span></span>

### <span data-ttu-id="9d0da-110">--------------------------Beispiel 1: Abrufen eines Netzwerkmonitors--------------------------</span><span class="sxs-lookup"><span data-stu-id="9d0da-110">--------------------------  Example 1: Get a Network Watcher  --------------------------</span></span>
```
Get-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

<span data-ttu-id="9d0da-111">Ruft den Netzwerkmonitor mit dem Namen NetworkWatcher_westcentralus in der Ressourcengruppe NetworkWatcherRG ab.</span><span class="sxs-lookup"><span data-stu-id="9d0da-111">Gets the Network Watcher named NetworkWatcher_westcentralus in the resource group NetworkWatcherRG.</span></span>

## <span data-ttu-id="9d0da-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d0da-112">PARAMETERS</span></span>

### <span data-ttu-id="9d0da-113">-Name</span><span class="sxs-lookup"><span data-stu-id="9d0da-113">-Name</span></span>
<span data-ttu-id="9d0da-114">Der Name des Netzwerkmonitors.</span><span class="sxs-lookup"><span data-stu-id="9d0da-114">The network watcher name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d0da-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d0da-115">-ResourceGroupName</span></span>
<span data-ttu-id="9d0da-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9d0da-116">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d0da-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d0da-117">-DefaultProfile</span></span>
<span data-ttu-id="9d0da-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9d0da-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d0da-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d0da-119">CommonParameters</span></span>
<span data-ttu-id="9d0da-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d0da-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d0da-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d0da-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d0da-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9d0da-122">INPUTS</span></span>

### <span data-ttu-id="9d0da-123">Keine</span><span class="sxs-lookup"><span data-stu-id="9d0da-123">None</span></span>

## <span data-ttu-id="9d0da-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9d0da-124">OUTPUTS</span></span>

### <span data-ttu-id="9d0da-125">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9d0da-125">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="9d0da-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="9d0da-126">NOTES</span></span>
<span data-ttu-id="9d0da-127">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Netzwerk, Netzwerke, Netzwerkmonitor</span><span class="sxs-lookup"><span data-stu-id="9d0da-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span> 

## <span data-ttu-id="9d0da-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9d0da-128">RELATED LINKS</span></span>

[<span data-ttu-id="9d0da-129">Neu – AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9d0da-129">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="9d0da-130">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9d0da-130">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="9d0da-131">Neu – AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9d0da-131">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9d0da-132">Neu – AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="9d0da-132">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="9d0da-133">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9d0da-133">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9d0da-134">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9d0da-134">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9d0da-135">Stopp-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9d0da-135">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9d0da-136">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="9d0da-136">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="9d0da-137">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="9d0da-137">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="9d0da-138">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="9d0da-138">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="9d0da-139">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="9d0da-139">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="9d0da-140">Anfang-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="9d0da-140">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
