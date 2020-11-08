---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 9996a42311ebfdf523b12822c1550b2faa78b6b0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003585"
---
# <span data-ttu-id="491f3-101">Get-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="491f3-101">Get-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="491f3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="491f3-102">SYNOPSIS</span></span>
<span data-ttu-id="491f3-103">Ruft eine Express Route Circuit Peering-Konfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="491f3-103">Gets an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="491f3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="491f3-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="491f3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="491f3-105">DESCRIPTION</span></span>
<span data-ttu-id="491f3-106">Das Cmdlet " **Get-AzExpressRouteCircuitPeeringConfig** " Ruft die Konfiguration einer Peering-Beziehung für einen Express Route-Schaltkreis ab.</span><span class="sxs-lookup"><span data-stu-id="491f3-106">The **Get-AzExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="491f3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="491f3-107">EXAMPLES</span></span>

### <span data-ttu-id="491f3-108">Beispiel 1: Anzeigen der Peering-Konfiguration für einen Express Route-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="491f3-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="491f3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="491f3-109">PARAMETERS</span></span>

### <span data-ttu-id="491f3-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="491f3-110">-DefaultProfile</span></span>
<span data-ttu-id="491f3-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="491f3-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="491f3-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="491f3-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="491f3-113">Das Express Route-Schaltkreis Objekt, das die Peering-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="491f3-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

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

### <span data-ttu-id="491f3-114">-Name</span><span class="sxs-lookup"><span data-stu-id="491f3-114">-Name</span></span>
<span data-ttu-id="491f3-115">Der Name der Peering-Konfiguration, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="491f3-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="491f3-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="491f3-116">CommonParameters</span></span>
<span data-ttu-id="491f3-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="491f3-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="491f3-118">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="491f3-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="491f3-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="491f3-119">INPUTS</span></span>

### <span data-ttu-id="491f3-120">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="491f3-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="491f3-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="491f3-121">OUTPUTS</span></span>

### <span data-ttu-id="491f3-122">Microsoft. Azure. Commands. Network. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="491f3-122">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="491f3-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="491f3-123">NOTES</span></span>

## <span data-ttu-id="491f3-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="491f3-124">RELATED LINKS</span></span>

[<span data-ttu-id="491f3-125">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="491f3-125">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="491f3-126">Neu – AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="491f3-126">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="491f3-127">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="491f3-127">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="491f3-128">Satz-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="491f3-128">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
