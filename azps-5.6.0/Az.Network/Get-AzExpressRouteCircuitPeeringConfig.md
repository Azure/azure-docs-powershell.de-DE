---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 7da632a1496b22e2f0be183640995a2aaa96735e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946507"
---
# <span data-ttu-id="4bdc7-101">Get-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="4bdc7-101">Get-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="4bdc7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bdc7-102">SYNOPSIS</span></span>
<span data-ttu-id="4bdc7-103">Ruft eine ExpressRoute-Peeringkonfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="4bdc7-103">Gets an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="4bdc7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4bdc7-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bdc7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4bdc7-105">DESCRIPTION</span></span>
<span data-ttu-id="4bdc7-106">Das **Get-AzExpressRouteCircuitPeeringConfig-Cmdlet** ruft die Konfiguration einer Peeringbeziehung für einen ExpressRoute-Schaltkreis ab.</span><span class="sxs-lookup"><span data-stu-id="4bdc7-106">The **Get-AzExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="4bdc7-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4bdc7-107">EXAMPLES</span></span>

### <span data-ttu-id="4bdc7-108">Beispiel 1: Anzeigen der Peeringkonfiguration für einen ExpressRoute-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="4bdc7-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="4bdc7-109">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4bdc7-109">PARAMETERS</span></span>

### <span data-ttu-id="4bdc7-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bdc7-110">-DefaultProfile</span></span>
<span data-ttu-id="4bdc7-111">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4bdc7-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bdc7-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4bdc7-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="4bdc7-113">Das ExpressRoute-Schaltkreisobjekt, das die Peeringkonfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="4bdc7-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

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

### <span data-ttu-id="4bdc7-114">-Name</span><span class="sxs-lookup"><span data-stu-id="4bdc7-114">-Name</span></span>
<span data-ttu-id="4bdc7-115">Der Name der abzurufenden Peeringkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="4bdc7-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="4bdc7-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bdc7-116">CommonParameters</span></span>
<span data-ttu-id="4bdc7-117">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bdc7-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bdc7-118">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4bdc7-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bdc7-119">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4bdc7-119">INPUTS</span></span>

### <span data-ttu-id="4bdc7-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4bdc7-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="4bdc7-121">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4bdc7-121">OUTPUTS</span></span>

### <span data-ttu-id="4bdc7-122">Microsoft.Azure.Commands.Network.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="4bdc7-122">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="4bdc7-123">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4bdc7-123">NOTES</span></span>

## <span data-ttu-id="4bdc7-124">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4bdc7-124">RELATED LINKS</span></span>

[<span data-ttu-id="4bdc7-125">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="4bdc7-125">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="4bdc7-126">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="4bdc7-126">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="4bdc7-127">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="4bdc7-127">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="4bdc7-128">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4bdc7-128">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
