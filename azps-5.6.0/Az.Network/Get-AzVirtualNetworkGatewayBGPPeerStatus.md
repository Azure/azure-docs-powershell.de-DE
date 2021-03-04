---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewaybgppeerstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayBGPPeerStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayBGPPeerStatus.md
ms.openlocfilehash: fd0bb4c3035eb2def0a1d0fa64038299cee4ec48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924752"
---
# <span data-ttu-id="800e7-101">Get-AzVirtualNetworkGatewayBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="800e7-101">Get-AzVirtualNetworkGatewayBGPPeerStatus</span></span>

## <span data-ttu-id="800e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="800e7-102">SYNOPSIS</span></span>
<span data-ttu-id="800e7-103">Listet die BGP-Peers eines Azure Virtual Network Gateways auf.</span><span class="sxs-lookup"><span data-stu-id="800e7-103">Lists an Azure virtual network gateway's BGP peers</span></span>

## <span data-ttu-id="800e7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="800e7-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-Peer <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="800e7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="800e7-105">DESCRIPTION</span></span>
<span data-ttu-id="800e7-106">Mit diesem Befehl werden BGP-Peers aufgezählt, für die ein Azure Virtual Network Gateway für Peers konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="800e7-106">This command enumerates BGP peers an Azure virtual network gateway is configured to peer with.</span></span> <span data-ttu-id="800e7-107">Der Status jedes Peers wird ebenfalls angegeben.</span><span class="sxs-lookup"><span data-stu-id="800e7-107">The status of each peer is also given.</span></span>

## <span data-ttu-id="800e7-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="800e7-108">EXAMPLES</span></span>

### <span data-ttu-id="800e7-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="800e7-109">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayBgpPeerStatus -ResourceGroupName resourceGroup -VirtualNetworkGatewayName gatewayName

Asn               : 65515
ConnectedDuration : 9.01:04:53.5768637
LocalAddress      : 10.1.0.254
MessagesReceived  : 14893
MessagesSent      : 14900
Neighbor          : 10.0.0.254
RoutesReceived    : 1
State             : Connected
```

<span data-ttu-id="800e7-110">Ruft BGP-Peers für das Azure Virtual Network Gateway namens gatewayName in resource group resourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="800e7-110">Retrieves BGP peers for the Azure virtual network gateway named gatewayName in resource group resourceGroup.</span></span>
<span data-ttu-id="800e7-111">Diese Beispielausgabe zeigt einen verbundenen BGP-Peer mit einer IP von 10.0.0.254.</span><span class="sxs-lookup"><span data-stu-id="800e7-111">This example output shows one connected BGP peer, with an IP of 10.0.0.254.</span></span>

## <span data-ttu-id="800e7-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="800e7-112">PARAMETERS</span></span>

### <span data-ttu-id="800e7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="800e7-113">-AsJob</span></span>
<span data-ttu-id="800e7-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="800e7-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="800e7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="800e7-115">-DefaultProfile</span></span>
<span data-ttu-id="800e7-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="800e7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="800e7-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="800e7-117">-Peer</span></span>
<span data-ttu-id="800e7-118">IP des Peers zum Abrufen des Status für</span><span class="sxs-lookup"><span data-stu-id="800e7-118">IP of the peer to retrieve status for</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="800e7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="800e7-119">-ResourceGroupName</span></span>
<span data-ttu-id="800e7-120">Name der Ressourcengruppe "Virtuelles Netzwerkgateway"</span><span class="sxs-lookup"><span data-stu-id="800e7-120">Virtual network gateway resource group's name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="800e7-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="800e7-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="800e7-122">Name des Virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="800e7-122">Virtual network gateway name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="800e7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="800e7-123">CommonParameters</span></span>
<span data-ttu-id="800e7-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="800e7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="800e7-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="800e7-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="800e7-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="800e7-126">INPUTS</span></span>

### <span data-ttu-id="800e7-127">System.String</span><span class="sxs-lookup"><span data-stu-id="800e7-127">System.String</span></span>

## <span data-ttu-id="800e7-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="800e7-128">OUTPUTS</span></span>

### <span data-ttu-id="800e7-129">Microsoft.Azure.Commands.Network.Models.PSBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="800e7-129">Microsoft.Azure.Commands.Network.Models.PSBGPPeerStatus</span></span>

## <span data-ttu-id="800e7-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="800e7-130">NOTES</span></span>

## <span data-ttu-id="800e7-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="800e7-131">RELATED LINKS</span></span>
