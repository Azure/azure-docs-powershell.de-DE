---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 0a0d23824b82b6a150b9547ef41c106ef237671b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366861"
---
# <span data-ttu-id="4aed3-101">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="4aed3-101">Remove-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="4aed3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4aed3-102">SYNOPSIS</span></span>
<span data-ttu-id="4aed3-103">Entfernt eine Konfiguration für Das Peering von ExpressRoute-Schaltkreisen.</span><span class="sxs-lookup"><span data-stu-id="4aed3-103">Removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="4aed3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4aed3-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4aed3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4aed3-105">DESCRIPTION</span></span>
<span data-ttu-id="4aed3-106">Das **Cmdlet "Remove-AzExpressRouteCircuitPeeringConfig"** entfernt eine ExpressRoute-Schaltkreispeerkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="4aed3-106">The **Remove-AzExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="4aed3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4aed3-107">EXAMPLES</span></span>

### <span data-ttu-id="4aed3-108">Beispiel 1: Entfernen einer Peeringkonfiguration aus einem "ExpressRoute"-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="4aed3-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="4aed3-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4aed3-109">PARAMETERS</span></span>

### <span data-ttu-id="4aed3-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aed3-110">-DefaultProfile</span></span>
<span data-ttu-id="4aed3-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4aed3-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4aed3-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4aed3-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="4aed3-113">Der ExpressRoute-Schaltkreis, der die zu entfernende Peeringkonfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="4aed3-113">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="4aed3-114">-Name</span><span class="sxs-lookup"><span data-stu-id="4aed3-114">-Name</span></span>
<span data-ttu-id="4aed3-115">Der Name der Peeringkonfiguration, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4aed3-115">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="4aed3-116">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="4aed3-116">-PeerAddressType</span></span>
<span data-ttu-id="4aed3-117">Die Adressfamilie des Peerings</span><span class="sxs-lookup"><span data-stu-id="4aed3-117">The Address family of the peering</span></span>

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

### <span data-ttu-id="4aed3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aed3-118">CommonParameters</span></span>
<span data-ttu-id="4aed3-119">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4aed3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aed3-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4aed3-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aed3-121">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4aed3-121">INPUTS</span></span>

### <span data-ttu-id="4aed3-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4aed3-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="4aed3-123">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4aed3-123">OUTPUTS</span></span>

### <span data-ttu-id="4aed3-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4aed3-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="4aed3-125">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4aed3-125">NOTES</span></span>

## <span data-ttu-id="4aed3-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4aed3-126">RELATED LINKS</span></span>

[<span data-ttu-id="4aed3-127">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="4aed3-127">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="4aed3-128">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4aed3-128">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="4aed3-129">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="4aed3-129">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="4aed3-130">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4aed3-130">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
