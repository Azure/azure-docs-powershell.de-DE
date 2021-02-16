---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
ms.openlocfilehash: 0004d43d802e89da51035727aae258181e38b00e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161124"
---
# <span data-ttu-id="13193-101">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="13193-101">Get-AzExpressRouteCircuitRouteTableSummary</span></span>

## <span data-ttu-id="13193-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13193-102">SYNOPSIS</span></span>
<span data-ttu-id="13193-103">Ruft eine Routentabelle mit einer Zusammenfassung eines ExpressRoute-Schaltkreises ab.</span><span class="sxs-lookup"><span data-stu-id="13193-103">Gets a route table summary of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="13193-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="13193-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="13193-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="13193-105">DESCRIPTION</span></span>
<span data-ttu-id="13193-106">Das **Cmdlet "Get-AzExpressRouteCircuitRouteTableSummary"** ruft eine Zusammenfassung der BGP-Benachbarten Informationen für einen bestimmten Routingkontext ab.</span><span class="sxs-lookup"><span data-stu-id="13193-106">The **Get-AzExpressRouteCircuitRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="13193-107">Diese Informationen sind hilfreich, um zu ermitteln, wie lange ein Routingkontext eingerichtet wurde und wie viele Routenpräfixe vom Peeringrouter angekündigt werden.</span><span class="sxs-lookup"><span data-stu-id="13193-107">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="13193-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="13193-108">EXAMPLES</span></span>

### <span data-ttu-id="13193-109">Beispiel 1: Anzeigen der Routenzusammenfassung für den primären Pfad</span><span class="sxs-lookup"><span data-stu-id="13193-109">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="13193-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13193-110">PARAMETERS</span></span>

### <span data-ttu-id="13193-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13193-111">-DefaultProfile</span></span>
<span data-ttu-id="13193-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="13193-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13193-113">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="13193-113">-DevicePath</span></span>
<span data-ttu-id="13193-114">Die zulässigen Werte für diesen Parameter `Primary` sind: `Secondary`</span><span class="sxs-lookup"><span data-stu-id="13193-114">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.DevicePathEnum
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13193-115">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="13193-115">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="13193-116">Der Name des zu untersuchende ExpressRoute-Schaltkreises.</span><span class="sxs-lookup"><span data-stu-id="13193-116">The name of the ExpressRoute circuit being examined.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13193-117">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="13193-117">-PeeringType</span></span>
<span data-ttu-id="13193-118">Die zulässigen Werte für diesen Parameter sind: `AzurePrivatePeering` `AzurePublicPeering` , und `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="13193-118">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13193-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13193-119">-ResourceGroupName</span></span>
<span data-ttu-id="13193-120">Der Name der Ressourcengruppe, die den "ExpressRoute"-Schaltkreis enthält.</span><span class="sxs-lookup"><span data-stu-id="13193-120">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="13193-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13193-121">CommonParameters</span></span>
<span data-ttu-id="13193-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13193-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13193-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13193-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13193-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="13193-124">INPUTS</span></span>

### <span data-ttu-id="13193-125">System.String</span><span class="sxs-lookup"><span data-stu-id="13193-125">System.String</span></span>

## <span data-ttu-id="13193-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="13193-126">OUTPUTS</span></span>

### <span data-ttu-id="13193-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span><span class="sxs-lookup"><span data-stu-id="13193-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span></span>

## <span data-ttu-id="13193-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="13193-128">NOTES</span></span>

## <span data-ttu-id="13193-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="13193-129">RELATED LINKS</span></span>

[<span data-ttu-id="13193-130">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="13193-130">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="13193-131">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="13193-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="13193-132">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="13193-132">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
