---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
ms.openlocfilehash: c27ac0c2a56000465b70810ca1e957b882fa3357
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921096"
---
# <span data-ttu-id="c34c4-101">Get-AzExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="c34c4-101">Get-AzExpressRouteServiceProvider</span></span>

## <span data-ttu-id="c34c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c34c4-102">SYNOPSIS</span></span>
<span data-ttu-id="c34c4-103">Ruft eine Liste der ExpressRoute-Dienstanbieter und deren Attribute ab.</span><span class="sxs-lookup"><span data-stu-id="c34c4-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

## <span data-ttu-id="c34c4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c34c4-104">SYNTAX</span></span>

```
Get-AzExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c34c4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c34c4-105">DESCRIPTION</span></span>
<span data-ttu-id="c34c4-106">Das **Get-AzExpressRouteServiceProvider-Cmdlet** ruft eine Liste von ExpressRoute-Dienstanbietern und deren Attributen ab.</span><span class="sxs-lookup"><span data-stu-id="c34c4-106">The **Get-AzExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="c34c4-107">Attribute umfassen Standort- und Bandbreitenoptionen.</span><span class="sxs-lookup"><span data-stu-id="c34c4-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="c34c4-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c34c4-108">EXAMPLES</span></span>

### <span data-ttu-id="c34c4-109">Beispiel 1: Erhalten einer Liste von Dienstanbietern mit Standorten im "Silicon Valley"</span><span class="sxs-lookup"><span data-stu-id="c34c4-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="c34c4-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c34c4-110">PARAMETERS</span></span>

### <span data-ttu-id="c34c4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c34c4-111">-DefaultProfile</span></span>
<span data-ttu-id="c34c4-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c34c4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c34c4-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c34c4-113">CommonParameters</span></span>
<span data-ttu-id="c34c4-114">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c34c4-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c34c4-115">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c34c4-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c34c4-116">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c34c4-116">INPUTS</span></span>

### <span data-ttu-id="c34c4-117">Keine</span><span class="sxs-lookup"><span data-stu-id="c34c4-117">None</span></span>

## <span data-ttu-id="c34c4-118">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c34c4-118">OUTPUTS</span></span>

### <span data-ttu-id="c34c4-119">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="c34c4-119">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="c34c4-120">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c34c4-120">NOTES</span></span>

## <span data-ttu-id="c34c4-121">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c34c4-121">RELATED LINKS</span></span>

[<span data-ttu-id="c34c4-122">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="c34c4-122">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="c34c4-123">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="c34c4-123">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="c34c4-124">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="c34c4-124">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="c34c4-125">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="c34c4-125">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
