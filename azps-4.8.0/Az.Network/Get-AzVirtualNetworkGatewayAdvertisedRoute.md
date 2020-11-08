---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayadvertisedroute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayAdvertisedRoute.md
ms.openlocfilehash: d41e71afc27129d2b2de40df97f12b0bb8f07ae5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165238"
---
# <span data-ttu-id="87d70-101">Get-AzVirtualNetworkGatewayAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="87d70-101">Get-AzVirtualNetworkGatewayAdvertisedRoute</span></span>

## <span data-ttu-id="87d70-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="87d70-102">SYNOPSIS</span></span>
<span data-ttu-id="87d70-103">Listet Routen auf, die von einem Azure Virtual Network Gateway angekündigt werden.</span><span class="sxs-lookup"><span data-stu-id="87d70-103">Lists routes being advertised by an Azure virtual network gateway</span></span>

## <span data-ttu-id="87d70-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="87d70-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -Peer <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87d70-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="87d70-105">DESCRIPTION</span></span>
<span data-ttu-id="87d70-106">Bei einer IP-Adresse eines BGP-Peers werden die Routen aufgelistet, die dem Peer vom angegebenen Azure Virtual Network-Gateway angekündigt werden.</span><span class="sxs-lookup"><span data-stu-id="87d70-106">Given the IP of a BGP peer, enumerates routes being advertised to that peer by the specified Azure virtual network gateway.</span></span> 

## <span data-ttu-id="87d70-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="87d70-107">EXAMPLES</span></span>

### <span data-ttu-id="87d70-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="87d70-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer 10.0.0.254
```

<span data-ttu-id="87d70-109">Ruft für das Azure-Gateway mit dem Namen Gatewayname in der Ressourcengruppe resourceGroupName eine Liste der Routen ab, die dem BGP-Peer mit IP-10.0.0.254 angekündigt werden.</span><span class="sxs-lookup"><span data-stu-id="87d70-109">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves a list of routes being advertised to the BGP peer with IP 10.0.0.254</span></span>

### <span data-ttu-id="87d70-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="87d70-110">Example 2</span></span>
```
PS C:\> $bgpPeerStatus = Get-AzVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName
PS C:\> Get-AzVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer $bgpPeerStatus[0].Neighbor
```

<span data-ttu-id="87d70-111">Ruft für das Azure-Gateway mit dem Namen Gatewayname in der Ressourcengruppe resourceGroupName die Routen ab, die für den ersten BGP-Peer in der Liste der BGP-Peers des Gateways angekündigt wurden.</span><span class="sxs-lookup"><span data-stu-id="87d70-111">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves routes being advertised to the first BGP peer on the gateway's list of BGP peers.</span></span>

## <span data-ttu-id="87d70-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="87d70-112">PARAMETERS</span></span>

### <span data-ttu-id="87d70-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="87d70-113">-AsJob</span></span>
<span data-ttu-id="87d70-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="87d70-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="87d70-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87d70-115">-DefaultProfile</span></span>
<span data-ttu-id="87d70-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="87d70-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87d70-117">-Peer</span><span class="sxs-lookup"><span data-stu-id="87d70-117">-Peer</span></span>
<span data-ttu-id="87d70-118">Die IP-Adresse des BGP-Peers.</span><span class="sxs-lookup"><span data-stu-id="87d70-118">BGP peer's IP address.</span></span> <span data-ttu-id="87d70-119">Hierbei sollte es sich um eine IP innerhalb des Adressbereichs handeln, auf den innerhalb des Azure Virtual Network, in dem das Gateway bereitgestellt wird, zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="87d70-119">This should be an IP within the address space accessible from within the Azure virtual network the gateway is deployed in.</span></span> 

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

### <span data-ttu-id="87d70-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87d70-120">-ResourceGroupName</span></span>
<span data-ttu-id="87d70-121">Name der Ressourcengruppe der virtuellen Netzwerk-Gateway-Ressource</span><span class="sxs-lookup"><span data-stu-id="87d70-121">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="87d70-122">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="87d70-122">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="87d70-123">Name des virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="87d70-123">Virtual network gateway name</span></span>

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

### <span data-ttu-id="87d70-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87d70-124">CommonParameters</span></span>
<span data-ttu-id="87d70-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87d70-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87d70-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87d70-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87d70-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="87d70-127">INPUTS</span></span>

### <span data-ttu-id="87d70-128">System. String</span><span class="sxs-lookup"><span data-stu-id="87d70-128">System.String</span></span>

## <span data-ttu-id="87d70-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="87d70-129">OUTPUTS</span></span>

### <span data-ttu-id="87d70-130">Microsoft. Azure. Commands. Network. Models. PSGatewayRoute</span><span class="sxs-lookup"><span data-stu-id="87d70-130">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute</span></span>

## <span data-ttu-id="87d70-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="87d70-131">NOTES</span></span>
<span data-ttu-id="87d70-132">Dieser Befehl gilt nur für Azure Virtual Network-Gateways mit BGP-aktivierten Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="87d70-132">This command is only applicable to Azure virtual network gateways with BGP enabled connections.</span></span>

## <span data-ttu-id="87d70-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="87d70-133">RELATED LINKS</span></span>
