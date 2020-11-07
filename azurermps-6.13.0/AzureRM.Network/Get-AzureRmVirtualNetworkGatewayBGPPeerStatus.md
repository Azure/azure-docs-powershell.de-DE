---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewaybgppeerstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayBGPPeerStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayBGPPeerStatus.md
ms.openlocfilehash: 4693b930714e70ad63dab25a4c8872feb5b92c21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665291"
---
# <span data-ttu-id="e8d74-101">Get-AzureRmVirtualNetworkGatewayBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="e8d74-101">Get-AzureRmVirtualNetworkGatewayBGPPeerStatus</span></span>

## <span data-ttu-id="e8d74-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e8d74-102">SYNOPSIS</span></span>
<span data-ttu-id="e8d74-103">Listet die BGP-Peers eines Azure Virtual Network-Gateways auf</span><span class="sxs-lookup"><span data-stu-id="e8d74-103">Lists an Azure virtual network gateway's BGP peers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8d74-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8d74-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 [-Peer <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8d74-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e8d74-105">DESCRIPTION</span></span>
<span data-ttu-id="e8d74-106">Dieser Befehl listet BGP-Peers auf, für die ein Azure Virtual Network Gateway für Peer konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="e8d74-106">This command enumerates BGP peers an Azure virtual network gateway is configured to peer with.</span></span> <span data-ttu-id="e8d74-107">Der Status jedes Peers wird ebenfalls angegeben.</span><span class="sxs-lookup"><span data-stu-id="e8d74-107">The status of each peer is also given.</span></span>

## <span data-ttu-id="e8d74-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e8d74-108">EXAMPLES</span></span>

### <span data-ttu-id="e8d74-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e8d74-109">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewayBgpPeerStatus -ResourceGroupName resourceGroup -VirtualNetworkGatewayName gatewayName

Asn               : 65515
ConnectedDuration : 9.01:04:53.5768637
LocalAddress      : 10.1.0.254
MessagesReceived  : 14893
MessagesSent      : 14900
Neighbor          : 10.0.0.254
RoutesReceived    : 1
State             : Connected
```

<span data-ttu-id="e8d74-110">Ruft BGP-Peers für das Azure Virtual Network Gateway mit dem Namen "Gatewayname" in der Ressourcengruppe "ResourceGroup" ab.</span><span class="sxs-lookup"><span data-stu-id="e8d74-110">Retrieves BGP peers for the Azure virtual network gateway named gatewayName in resource group resourceGroup.</span></span>
<span data-ttu-id="e8d74-111">Diese Beispielausgabe zeigt einen verbundenen BGP-Peer mit einer IP-Adresse von 10.0.0.254.</span><span class="sxs-lookup"><span data-stu-id="e8d74-111">This example output shows one connected BGP peer, with an IP of 10.0.0.254.</span></span>

## <span data-ttu-id="e8d74-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8d74-112">PARAMETERS</span></span>

### <span data-ttu-id="e8d74-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e8d74-113">-AsJob</span></span>
<span data-ttu-id="e8d74-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e8d74-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e8d74-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8d74-115">-DefaultProfile</span></span>
<span data-ttu-id="e8d74-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e8d74-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8d74-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="e8d74-117">-Peer</span></span>
<span data-ttu-id="e8d74-118">Die IP-Adresse des Peers, für den der Status abgerufen werden soll</span><span class="sxs-lookup"><span data-stu-id="e8d74-118">IP of the peer to retrieve status for</span></span>

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

### <span data-ttu-id="e8d74-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8d74-119">-ResourceGroupName</span></span>
<span data-ttu-id="e8d74-120">Name der Ressourcengruppe der virtuellen Netzwerk-Gateway-Ressource</span><span class="sxs-lookup"><span data-stu-id="e8d74-120">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="e8d74-121">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="e8d74-121">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="e8d74-122">Name des virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="e8d74-122">Virtual network gateway name</span></span>

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

### <span data-ttu-id="e8d74-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8d74-123">CommonParameters</span></span>
<span data-ttu-id="e8d74-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8d74-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8d74-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8d74-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8d74-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e8d74-126">INPUTS</span></span>

### <span data-ttu-id="e8d74-127">System. String</span><span class="sxs-lookup"><span data-stu-id="e8d74-127">System.String</span></span>

## <span data-ttu-id="e8d74-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e8d74-128">OUTPUTS</span></span>

### <span data-ttu-id="e8d74-129">Microsoft. Azure. Commands. Network. Models. PSBGPPeerStatus</span><span class="sxs-lookup"><span data-stu-id="e8d74-129">Microsoft.Azure.Commands.Network.Models.PSBGPPeerStatus</span></span>

## <span data-ttu-id="e8d74-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="e8d74-130">NOTES</span></span>

## <span data-ttu-id="e8d74-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e8d74-131">RELATED LINKS</span></span>
