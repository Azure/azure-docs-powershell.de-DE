---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 009F6E65-0268-4505-AEC1-FF379CB96804
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteserviceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteServiceProvider.md
ms.openlocfilehash: 5e0464a4266a68905da26859f20faca918a9caab
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98300792"
---
# <span data-ttu-id="b02ae-101">Get-AzExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="b02ae-101">Get-AzExpressRouteServiceProvider</span></span>

## <span data-ttu-id="b02ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b02ae-102">SYNOPSIS</span></span>
<span data-ttu-id="b02ae-103">Ruft eine Liste der ExpressRoute-Dienstanbieter und deren Attribute ab.</span><span class="sxs-lookup"><span data-stu-id="b02ae-103">Gets a list ExpressRoute service providers and their attributes.</span></span>

## <span data-ttu-id="b02ae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b02ae-104">SYNTAX</span></span>

```
Get-AzExpressRouteServiceProvider [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b02ae-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b02ae-105">DESCRIPTION</span></span>
<span data-ttu-id="b02ae-106">Das **Cmdlet "Get-AzExpressRouteServiceProvider"** ruft eine Liste der ExpressRoute-Dienstanbieter und deren Attribute ab.</span><span class="sxs-lookup"><span data-stu-id="b02ae-106">The **Get-AzExpressRouteServiceProvider** cmdlet retrieves a list ExpressRoute service providers and their attributes.</span></span> <span data-ttu-id="b02ae-107">Zu den Attributen gehören Standort- und Bandbreitenoptionen.</span><span class="sxs-lookup"><span data-stu-id="b02ae-107">Attribute include location and bandwidth options.</span></span>

## <span data-ttu-id="b02ae-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b02ae-108">EXAMPLES</span></span>

### <span data-ttu-id="b02ae-109">Beispiel 1: Erhalten einer Liste des Dienstanbieters mit Standorten in "Silicon Valley"</span><span class="sxs-lookup"><span data-stu-id="b02ae-109">Example 1: Get a list of service provider with locations in "Silicon Valley"</span></span>
```
Get-AzExpressRouteServiceProvider |
   Where-Object PeeringLocations -Contains "Silicon Valley" |
   Select-Object Name
```

## <span data-ttu-id="b02ae-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b02ae-110">PARAMETERS</span></span>

### <span data-ttu-id="b02ae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b02ae-111">-DefaultProfile</span></span>
<span data-ttu-id="b02ae-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b02ae-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b02ae-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b02ae-113">CommonParameters</span></span>
<span data-ttu-id="b02ae-114">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b02ae-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b02ae-115">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b02ae-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b02ae-116">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b02ae-116">INPUTS</span></span>

### <span data-ttu-id="b02ae-117">Keine</span><span class="sxs-lookup"><span data-stu-id="b02ae-117">None</span></span>

## <span data-ttu-id="b02ae-118">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b02ae-118">OUTPUTS</span></span>

### <span data-ttu-id="b02ae-119">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span><span class="sxs-lookup"><span data-stu-id="b02ae-119">Microsoft.Azure.Commands.Network.Models.PSExpressRouteServiceProvider</span></span>

## <span data-ttu-id="b02ae-120">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b02ae-120">NOTES</span></span>

## <span data-ttu-id="b02ae-121">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b02ae-121">RELATED LINKS</span></span>

[<span data-ttu-id="b02ae-122">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="b02ae-122">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="b02ae-123">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="b02ae-123">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="b02ae-124">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b02ae-124">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="b02ae-125">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="b02ae-125">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
