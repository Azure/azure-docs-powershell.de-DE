---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 187921598b21747764436dd4ae6f988961d4a951
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941675"
---
# <span data-ttu-id="37aba-101">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="37aba-101">Remove-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="37aba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37aba-102">SYNOPSIS</span></span>
<span data-ttu-id="37aba-103">Entfernt eine ExpressRoute-Schaltkreis-Peeringkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="37aba-103">Removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="37aba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="37aba-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37aba-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="37aba-105">DESCRIPTION</span></span>
<span data-ttu-id="37aba-106">Das **Cmdlet Remove-AzExpressRouteCircuitPeeringConfig** entfernt eine ExpressRoute-Peeringkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="37aba-106">The **Remove-AzExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="37aba-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="37aba-107">EXAMPLES</span></span>

### <span data-ttu-id="37aba-108">Beispiel 1: Entfernen einer Peeringkonfiguration aus einem ExpressRoute-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="37aba-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="37aba-109">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="37aba-109">PARAMETERS</span></span>

### <span data-ttu-id="37aba-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37aba-110">-DefaultProfile</span></span>
<span data-ttu-id="37aba-111">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="37aba-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37aba-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="37aba-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="37aba-113">Der ExpressRoute-Schaltkreis, der die zu entfernende Peeringkonfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="37aba-113">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="37aba-114">-Name</span><span class="sxs-lookup"><span data-stu-id="37aba-114">-Name</span></span>
<span data-ttu-id="37aba-115">Der Name der peering-Konfiguration, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="37aba-115">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="37aba-116">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="37aba-116">-PeerAddressType</span></span>
<span data-ttu-id="37aba-117">Die Adressfamilie des Peerings</span><span class="sxs-lookup"><span data-stu-id="37aba-117">The Address family of the peering</span></span>

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

### <span data-ttu-id="37aba-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37aba-118">CommonParameters</span></span>
<span data-ttu-id="37aba-119">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37aba-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37aba-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37aba-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37aba-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="37aba-121">INPUTS</span></span>

### <span data-ttu-id="37aba-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="37aba-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="37aba-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="37aba-123">OUTPUTS</span></span>

### <span data-ttu-id="37aba-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="37aba-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="37aba-125">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="37aba-125">NOTES</span></span>

## <span data-ttu-id="37aba-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="37aba-126">RELATED LINKS</span></span>

[<span data-ttu-id="37aba-127">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="37aba-127">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="37aba-128">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="37aba-128">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="37aba-129">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="37aba-129">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="37aba-130">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="37aba-130">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
