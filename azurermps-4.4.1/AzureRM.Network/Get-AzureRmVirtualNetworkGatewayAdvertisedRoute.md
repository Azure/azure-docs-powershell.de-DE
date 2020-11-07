---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayAdvertisedRoute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayAdvertisedRoute.md
ms.openlocfilehash: a9b8cd9f13de8c1c4e3a7f20a0ffe410211f8973
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662968"
---
# <span data-ttu-id="faa3e-101">Get-AzureRmVirtualNetworkGatewayAdvertisedRoute</span><span class="sxs-lookup"><span data-stu-id="faa3e-101">Get-AzureRmVirtualNetworkGatewayAdvertisedRoute</span></span>

## <span data-ttu-id="faa3e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="faa3e-102">SYNOPSIS</span></span>
<span data-ttu-id="faa3e-103">Listet Routen auf, die von einem Azure Virtual Network Gateway angekündigt werden.</span><span class="sxs-lookup"><span data-stu-id="faa3e-103">Lists routes being advertised by an Azure virtual network gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="faa3e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="faa3e-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName <String> -ResourceGroupName <String>
 -Peer <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="faa3e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="faa3e-105">DESCRIPTION</span></span>
<span data-ttu-id="faa3e-106">Bei einer IP-Adresse eines BGP-Peers werden die Routen aufgelistet, die dem Peer vom angegebenen Azure Virtual Network-Gateway angekündigt werden.</span><span class="sxs-lookup"><span data-stu-id="faa3e-106">Given the IP of a BGP peer, enumerates routes being advertised to that peer by the specified Azure virtual network gateway.</span></span> 

## <span data-ttu-id="faa3e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="faa3e-107">EXAMPLES</span></span>

### <span data-ttu-id="faa3e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="faa3e-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer 10.0.0.254
```

<span data-ttu-id="faa3e-109">Für das Azure-Gateway mit dem Namen Gatewayname in der Ressourcengruppe resourceGroupName retrives eine Liste der Routen, die dem BGP-Peer mit IP-10.0.0.254 angekündigt werden.</span><span class="sxs-lookup"><span data-stu-id="faa3e-109">For the Azure gateway named gatewayName in resource group resourceGroupName, retrives a list of routes being advertised to the BGP peer with IP 10.0.0.254</span></span>

### <span data-ttu-id="faa3e-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="faa3e-110">Example 2</span></span>
```
PS C:\> $bgpPeerStatus = Get-AzureRmVirtualNetworkGatewayBGPPeerStatus -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName
PS C:\> Get-AzureRmVirtualNetworkGatewayAdvertisedRoute -VirtualNetworkGatewayName gatewayName -ResourceGroupName resourceGroupName -Peer $bgpPeerStatus[0].Neighbor
```

<span data-ttu-id="faa3e-111">Ruft für das Azure-Gateway mit dem Namen Gatewayname in der Ressourcengruppe resourceGroupName die Routen ab, die für den ersten BGP-Peer in der Liste der BGP-Peers des Gateways angekündigt wurden.</span><span class="sxs-lookup"><span data-stu-id="faa3e-111">For the Azure gateway named gatewayName in resource group resourceGroupName, retrieves routes being advertised to the first BGP peer on the gateway's list of BGP peers.</span></span>

## <span data-ttu-id="faa3e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="faa3e-112">PARAMETERS</span></span>

### <span data-ttu-id="faa3e-113">-Peer</span><span class="sxs-lookup"><span data-stu-id="faa3e-113">-Peer</span></span>
<span data-ttu-id="faa3e-114">Die IP-Adresse des BGP-Peers.</span><span class="sxs-lookup"><span data-stu-id="faa3e-114">BGP peer's IP address.</span></span> <span data-ttu-id="faa3e-115">Hierbei sollte es sich um eine IP innerhalb des Adressbereichs handeln, auf den innerhalb des Azure Virtual Network, in dem das Gateway bereitgestellt wird, zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="faa3e-115">This should be an IP within the address space accessible from within the Azure virtual network the gateway is deployed in.</span></span> 

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

### <span data-ttu-id="faa3e-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="faa3e-116">-ResourceGroupName</span></span>
<span data-ttu-id="faa3e-117">Name der Ressourcengruppe der virtuellen Netzwerk-Gateway-Ressource</span><span class="sxs-lookup"><span data-stu-id="faa3e-117">Virtual network gateway resource group's name</span></span>

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

### <span data-ttu-id="faa3e-118">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="faa3e-118">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="faa3e-119">Name des virtuellen Netzwerkgateways</span><span class="sxs-lookup"><span data-stu-id="faa3e-119">Virtual network gateway name</span></span>

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

### <span data-ttu-id="faa3e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faa3e-120">-DefaultProfile</span></span>
<span data-ttu-id="faa3e-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="faa3e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="faa3e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faa3e-122">CommonParameters</span></span>
<span data-ttu-id="faa3e-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="faa3e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faa3e-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="faa3e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faa3e-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="faa3e-125">INPUTS</span></span>

### <span data-ttu-id="faa3e-126">System. String</span><span class="sxs-lookup"><span data-stu-id="faa3e-126">System.String</span></span>

## <span data-ttu-id="faa3e-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="faa3e-127">OUTPUTS</span></span>

### <span data-ttu-id="faa3e-128">Microsoft. Azure. Commands. Network. Models. PSGatewayRoute []</span><span class="sxs-lookup"><span data-stu-id="faa3e-128">Microsoft.Azure.Commands.Network.Models.PSGatewayRoute[]</span></span>

## <span data-ttu-id="faa3e-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="faa3e-129">NOTES</span></span>
<span data-ttu-id="faa3e-130">Dieser Befehl gilt nur für Azure Virtual Network-Gateways mit BGP-aktivierten Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="faa3e-130">This command is only applicable to Azure virtual network gateways with BGP enabled connections.</span></span>

## <span data-ttu-id="faa3e-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="faa3e-131">RELATED LINKS</span></span>

