---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: BA7F6BAC-6047-42B0-B8CA-0B36302951B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTable.md
ms.openlocfilehash: 4c93528c8cf89d64dd99640ce9eca4668d4093c0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154417"
---
# <span data-ttu-id="4ebac-101">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="4ebac-101">Get-AzExpressRouteCrossConnectionRouteTable</span></span>

## <span data-ttu-id="4ebac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ebac-102">SYNOPSIS</span></span>
<span data-ttu-id="4ebac-103">Ruft eine Routentabelle aus einer ExpressRoute-Kreuzverbindung ab.</span><span class="sxs-lookup"><span data-stu-id="4ebac-103">Gets a route table from an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="4ebac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ebac-104">SYNTAX</span></span>

### <span data-ttu-id="4ebac-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="4ebac-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4ebac-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="4ebac-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4ebac-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4ebac-107">DESCRIPTION</span></span>
<span data-ttu-id="4ebac-108">Das **Cmdlet "Get-AzExpressRouteCrossConnectionRouteTable"** ruft eine detaillierte Routentabelle eines ExpressRoute-Schaltkreises ab.</span><span class="sxs-lookup"><span data-stu-id="4ebac-108">The **Get-AzExpressRouteCrossConnectionRouteTable** cmdlet retrieves a detailed route table of an ExpressRoute circuit.</span></span> <span data-ttu-id="4ebac-109">In der Routentabelle werden alle Routen angezeigt oder können gefiltert werden, um Routen für einen bestimmten Peeringtyp zu zeigen.</span><span class="sxs-lookup"><span data-stu-id="4ebac-109">The route table will show all routes or can be filtered to show routes for a specific peering type.</span></span> <span data-ttu-id="4ebac-110">Sie können die Routentabelle verwenden, um Ihre Peeringkonfiguration und -konnektivität zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="4ebac-110">You can use the route table to validate your peering configuration and connectivity.</span></span>

## <span data-ttu-id="4ebac-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4ebac-111">EXAMPLES</span></span>

### <span data-ttu-id="4ebac-112">Beispiel 1: Anzeigen der Routentabelle für den primären Pfad</span><span class="sxs-lookup"><span data-stu-id="4ebac-112">Example 1: Display the route table for the primary path</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTable -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CircuitName -DevicePath 'Primary'
```

## <span data-ttu-id="4ebac-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ebac-113">PARAMETERS</span></span>

### <span data-ttu-id="4ebac-114">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="4ebac-114">-CrossConnectionName</span></span>
<span data-ttu-id="4ebac-115">Der Name der Express Route Cross Connection</span><span class="sxs-lookup"><span data-stu-id="4ebac-115">The Name of Express Route Cross Connection</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyByParameterValues
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ebac-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ebac-116">-DefaultProfile</span></span>
<span data-ttu-id="4ebac-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4ebac-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ebac-118">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="4ebac-118">-DevicePath</span></span>
<span data-ttu-id="4ebac-119">Die zulässigen Werte für diesen Parameter `Primary` sind: `Secondary`</span><span class="sxs-lookup"><span data-stu-id="4ebac-119">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="4ebac-120">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="4ebac-120">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="4ebac-121">Die Express Route Cross Connection</span><span class="sxs-lookup"><span data-stu-id="4ebac-121">The Express Route Cross Connection</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: SpecifyByReference
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ebac-122">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="4ebac-122">-PeeringType</span></span>
<span data-ttu-id="4ebac-123">Die zulässigen Werte für diesen Parameter sind: `AzurePrivatePeering` `AzurePublicPeering` , und `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="4ebac-123">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="4ebac-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ebac-124">-ResourceGroupName</span></span>
<span data-ttu-id="4ebac-125">Der Name der Ressourcengruppe, die die ExpressRoute-Querverbindung enthält.</span><span class="sxs-lookup"><span data-stu-id="4ebac-125">The name of the resource group containing the ExpressRoute cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ebac-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ebac-126">CommonParameters</span></span>
<span data-ttu-id="4ebac-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ebac-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ebac-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4ebac-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ebac-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4ebac-129">INPUTS</span></span>

### <span data-ttu-id="4ebac-130">Keine</span><span class="sxs-lookup"><span data-stu-id="4ebac-130">None</span></span>
<span data-ttu-id="4ebac-131">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="4ebac-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4ebac-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4ebac-132">OUTPUTS</span></span>

### <span data-ttu-id="4ebac-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span><span class="sxs-lookup"><span data-stu-id="4ebac-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitRoutesTable</span></span>

## <span data-ttu-id="4ebac-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4ebac-134">NOTES</span></span>

## <span data-ttu-id="4ebac-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4ebac-135">RELATED LINKS</span></span>

[<span data-ttu-id="4ebac-136">Get-AzExpressRouteCrossConnectionARPTable</span><span class="sxs-lookup"><span data-stu-id="4ebac-136">Get-AzExpressRouteCrossConnectionARPTable</span></span>](Get-AzExpressRouteCrossConnectionARPTable.md)

[<span data-ttu-id="4ebac-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="4ebac-137">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>](Get-AzExpressRouteCrossConnectionRouteTableSummary.md)
