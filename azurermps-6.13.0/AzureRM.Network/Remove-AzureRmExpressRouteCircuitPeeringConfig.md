---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 965ebd3fe81ced04aee88a6f5a9bbd427017a4e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505298"
---
# <span data-ttu-id="183f0-101">Remove-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="183f0-101">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="183f0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="183f0-102">SYNOPSIS</span></span>
<span data-ttu-id="183f0-103">Entfernt eine Express Route Circuit-Peering-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="183f0-103">Removes an ExpressRoute circuit peering configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="183f0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="183f0-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="183f0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="183f0-105">DESCRIPTION</span></span>
<span data-ttu-id="183f0-106">Das Cmdlet " **Remove-AzureRmExpressRouteCircuitPeeringConfig** " entfernt eine Express Route Circuit-Peering-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="183f0-106">The **Remove-AzureRmExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="183f0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="183f0-107">EXAMPLES</span></span>

### <span data-ttu-id="183f0-108">Beispiel 1: Entfernen einer Peering-Konfiguration von einem Express Route-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="183f0-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzureRmExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="183f0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="183f0-109">PARAMETERS</span></span>

### <span data-ttu-id="183f0-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="183f0-110">-DefaultProfile</span></span>
<span data-ttu-id="183f0-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="183f0-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="183f0-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="183f0-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="183f0-113">Der Express Route-Schaltkreis mit der Peering-Konfiguration, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="183f0-113">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="183f0-114">-Name</span><span class="sxs-lookup"><span data-stu-id="183f0-114">-Name</span></span>
<span data-ttu-id="183f0-115">Der Name der zu entfernende Peering-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="183f0-115">The name of the peering configuration to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="183f0-116">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="183f0-116">-PeerAddressType</span></span>
<span data-ttu-id="183f0-117">Die Adressfamilie des Peerings</span><span class="sxs-lookup"><span data-stu-id="183f0-117">The Address family of the peering</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="183f0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="183f0-118">CommonParameters</span></span>
<span data-ttu-id="183f0-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="183f0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="183f0-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="183f0-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="183f0-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="183f0-121">INPUTS</span></span>

### <span data-ttu-id="183f0-122">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="183f0-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="183f0-123">Parameter: ExpressRouteCircuit (ByValue)</span><span class="sxs-lookup"><span data-stu-id="183f0-123">Parameters: ExpressRouteCircuit (ByValue)</span></span>

## <span data-ttu-id="183f0-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="183f0-124">OUTPUTS</span></span>

### <span data-ttu-id="183f0-125">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="183f0-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="183f0-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="183f0-126">NOTES</span></span>

## <span data-ttu-id="183f0-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="183f0-127">RELATED LINKS</span></span>

[<span data-ttu-id="183f0-128">Add-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="183f0-128">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="183f0-129">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="183f0-129">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="183f0-130">Neu – AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="183f0-130">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="183f0-131">Satz-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="183f0-131">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
