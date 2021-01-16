---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 9996a42311ebfdf523b12822c1550b2faa78b6b0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291911"
---
# <span data-ttu-id="f00b9-101">Get-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="f00b9-101">Get-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="f00b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f00b9-102">SYNOPSIS</span></span>
<span data-ttu-id="f00b9-103">Ruft eine Konfiguration für das Peering von ExpressRoute-Schaltkreisen ab.</span><span class="sxs-lookup"><span data-stu-id="f00b9-103">Gets an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="f00b9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f00b9-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f00b9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f00b9-105">DESCRIPTION</span></span>
<span data-ttu-id="f00b9-106">Das **Cmdlet "Get-AzExpressRouteCircuitPeeringConfig"** ruft die Konfiguration einer Peeringbeziehung für einen "ExpressRoute"-Schaltkreis ab.</span><span class="sxs-lookup"><span data-stu-id="f00b9-106">The **Get-AzExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="f00b9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f00b9-107">EXAMPLES</span></span>

### <span data-ttu-id="f00b9-108">Beispiel 1: Anzeigen der Peeringkonfiguration für einen ExpressRoute-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="f00b9-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="f00b9-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f00b9-109">PARAMETERS</span></span>

### <span data-ttu-id="f00b9-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f00b9-110">-DefaultProfile</span></span>
<span data-ttu-id="f00b9-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f00b9-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f00b9-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f00b9-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="f00b9-113">Das ExpressRoute-Schaltkreisobjekt, das die Peeringkonfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="f00b9-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

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

### <span data-ttu-id="f00b9-114">-Name</span><span class="sxs-lookup"><span data-stu-id="f00b9-114">-Name</span></span>
<span data-ttu-id="f00b9-115">Der Name der abzurufenden Peeringkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="f00b9-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="f00b9-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f00b9-116">CommonParameters</span></span>
<span data-ttu-id="f00b9-117">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f00b9-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f00b9-118">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f00b9-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f00b9-119">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f00b9-119">INPUTS</span></span>

### <span data-ttu-id="f00b9-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f00b9-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="f00b9-121">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f00b9-121">OUTPUTS</span></span>

### <span data-ttu-id="f00b9-122">Microsoft.Azure.Commands.Network.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="f00b9-122">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="f00b9-123">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f00b9-123">NOTES</span></span>

## <span data-ttu-id="f00b9-124">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f00b9-124">RELATED LINKS</span></span>

[<span data-ttu-id="f00b9-125">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="f00b9-125">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="f00b9-126">New-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="f00b9-126">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="f00b9-127">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="f00b9-127">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="f00b9-128">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f00b9-128">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
