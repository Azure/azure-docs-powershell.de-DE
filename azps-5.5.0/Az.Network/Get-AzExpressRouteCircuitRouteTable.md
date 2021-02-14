---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitRouteTable.md
ms.openlocfilehash: 3067df10f3cd1d49b519d6c83defe304fbcf0296
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170015"
---
# <span data-ttu-id="0c0f9-101">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="0c0f9-101">Get-AzExpressRouteCircuitRouteTable</span></span>

## <span data-ttu-id="0c0f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c0f9-102">SYNOPSIS</span></span>
<span data-ttu-id="0c0f9-103">Ruft eine Routentabelle aus einem "ExpressRoute"-Schaltkreis ab.</span><span class="sxs-lookup"><span data-stu-id="0c0f9-103">Gets a route table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="0c0f9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0c0f9-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitRouteTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0c0f9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0c0f9-105">DESCRIPTION</span></span>
<span data-ttu-id="0c0f9-106">Das **Cmdlet "Get-AzExpressRouteCircuitRouteTable"** ruft eine detaillierte Routentabelle eines ExpressRoute-Schaltkreises ab.</span><span class="sxs-lookup"><span data-stu-id="0c0f9-106">The **Get-AzExpressRouteCircuitRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="0c0f9-107">In der Routentabelle werden alle Routen angezeigt oder können gefiltert werden, um Routen für einen bestimmten Peeringtyp zu zeigen.</span><span class="sxs-lookup"><span data-stu-id="0c0f9-107">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="0c0f9-108">Sie können die Routentabelle verwenden, um Ihre Peeringkonfiguration und -konnektivität zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="0c0f9-108">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="0c0f9-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0c0f9-109">EXAMPLES</span></span>

### <span data-ttu-id="0c0f9-110">Beispiel 1: Anzeigen der Routentabelle für den primären Pfad</span><span class="sxs-lookup"><span data-stu-id="0c0f9-110">Example 1: Display the route table for the primary path</span></span>
```
Get-AzExpressRouteCircuitRouteTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="0c0f9-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c0f9-111">PARAMETERS</span></span>

### <span data-ttu-id="0c0f9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c0f9-112">-DefaultProfile</span></span>
<span data-ttu-id="0c0f9-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0c0f9-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c0f9-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="0c0f9-114">-DevicePath</span></span>
<span data-ttu-id="0c0f9-115">Die zulässigen Werte für diesen Parameter `Primary` sind: `Secondary`</span><span class="sxs-lookup"><span data-stu-id="0c0f9-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="0c0f9-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="0c0f9-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="0c0f9-117">Der Name des zu untersuchende ExpressRoute-Schaltkreises.</span><span class="sxs-lookup"><span data-stu-id="0c0f9-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="0c0f9-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="0c0f9-118">-PeeringType</span></span>
<span data-ttu-id="0c0f9-119">Die zulässigen Werte für diesen Parameter sind: `AzurePrivatePeering` `AzurePublicPeering` , und `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="0c0f9-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="0c0f9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c0f9-120">-ResourceGroupName</span></span>
<span data-ttu-id="0c0f9-121">Der Name der Ressourcengruppe, die den "ExpressRoute"-Schaltkreis enthält.</span><span class="sxs-lookup"><span data-stu-id="0c0f9-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="0c0f9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c0f9-122">CommonParameters</span></span>
<span data-ttu-id="0c0f9-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c0f9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c0f9-124">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c0f9-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c0f9-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0c0f9-125">INPUTS</span></span>

### <span data-ttu-id="0c0f9-126">System.String</span><span class="sxs-lookup"><span data-stu-id="0c0f9-126">System.String</span></span>

## <span data-ttu-id="0c0f9-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0c0f9-127">OUTPUTS</span></span>

### <span data-ttu-id="0c0f9-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="0c0f9-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="0c0f9-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0c0f9-129">NOTES</span></span>

## <span data-ttu-id="0c0f9-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0c0f9-130">RELATED LINKS</span></span>

[<span data-ttu-id="0c0f9-131">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="0c0f9-131">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="0c0f9-132">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="0c0f9-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="0c0f9-133">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="0c0f9-133">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
