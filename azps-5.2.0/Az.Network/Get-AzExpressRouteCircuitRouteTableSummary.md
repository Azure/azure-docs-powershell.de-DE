---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTableSummary.md
ms.openlocfilehash: 0004d43d802e89da51035727aae258181e38b00e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98292642"
---
# <span data-ttu-id="2be59-101">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="2be59-101">Get-AzExpressRouteCircuitRouteTableSummary</span></span>

## <span data-ttu-id="2be59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2be59-102">SYNOPSIS</span></span>
<span data-ttu-id="2be59-103">Ruft eine Routentabelle mit einer Zusammenfassung eines ExpressRoute-Schaltkreises ab.</span><span class="sxs-lookup"><span data-stu-id="2be59-103">Gets a route table summary of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="2be59-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2be59-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2be59-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2be59-105">DESCRIPTION</span></span>
<span data-ttu-id="2be59-106">Das **Cmdlet "Get-AzExpressRouteCircuitRouteTableSummary"** ruft eine Zusammenfassung der BGP-Benachbarten Informationen für einen bestimmten Routingkontext ab.</span><span class="sxs-lookup"><span data-stu-id="2be59-106">The **Get-AzExpressRouteCircuitRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="2be59-107">Diese Informationen sind hilfreich, um zu ermitteln, wie lange ein Routingkontext eingerichtet wurde und wie viele Routenpräfixe vom Peeringrouter angekündigt werden.</span><span class="sxs-lookup"><span data-stu-id="2be59-107">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="2be59-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2be59-108">EXAMPLES</span></span>

### <span data-ttu-id="2be59-109">Beispiel 1: Anzeigen der Routenzusammenfassung für den primären Pfad</span><span class="sxs-lookup"><span data-stu-id="2be59-109">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTableSummary -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="2be59-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2be59-110">PARAMETERS</span></span>

### <span data-ttu-id="2be59-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2be59-111">-DefaultProfile</span></span>
<span data-ttu-id="2be59-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2be59-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2be59-113">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="2be59-113">-DevicePath</span></span>
<span data-ttu-id="2be59-114">Die zulässigen Werte für diesen Parameter `Primary` sind: `Secondary`</span><span class="sxs-lookup"><span data-stu-id="2be59-114">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="2be59-115">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="2be59-115">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="2be59-116">Der Name des zu untersuchende ExpressRoute-Schaltkreises.</span><span class="sxs-lookup"><span data-stu-id="2be59-116">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="2be59-117">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="2be59-117">-PeeringType</span></span>
<span data-ttu-id="2be59-118">Die zulässigen Werte für diesen Parameter sind: `AzurePrivatePeering` `AzurePublicPeering` , und `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="2be59-118">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="2be59-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2be59-119">-ResourceGroupName</span></span>
<span data-ttu-id="2be59-120">Der Name der Ressourcengruppe, die den "ExpressRoute"-Schaltkreis enthält.</span><span class="sxs-lookup"><span data-stu-id="2be59-120">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="2be59-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2be59-121">CommonParameters</span></span>
<span data-ttu-id="2be59-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2be59-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2be59-123">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2be59-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2be59-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2be59-124">INPUTS</span></span>

### <span data-ttu-id="2be59-125">System.String</span><span class="sxs-lookup"><span data-stu-id="2be59-125">System.String</span></span>

## <span data-ttu-id="2be59-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2be59-126">OUTPUTS</span></span>

### <span data-ttu-id="2be59-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span><span class="sxs-lookup"><span data-stu-id="2be59-127">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTableSummary</span></span>

## <span data-ttu-id="2be59-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2be59-128">NOTES</span></span>

## <span data-ttu-id="2be59-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2be59-129">RELATED LINKS</span></span>

[<span data-ttu-id="2be59-130">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="2be59-130">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="2be59-131">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="2be59-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="2be59-132">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="2be59-132">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
