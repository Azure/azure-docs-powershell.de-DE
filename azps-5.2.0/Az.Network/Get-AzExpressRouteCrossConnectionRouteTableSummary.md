---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecrossconnectionroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTableSummary.md
ms.openlocfilehash: 7479d18660ede3f70ac5e62f614b8a815b86433c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98292619"
---
# <span data-ttu-id="48c2c-101">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="48c2c-101">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

## <span data-ttu-id="48c2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48c2c-102">SYNOPSIS</span></span>
<span data-ttu-id="48c2c-103">Ruft eine Routentabelle mit einer Zusammenfassung einer ExpressRoute-Kreuzverbindung ab.</span><span class="sxs-lookup"><span data-stu-id="48c2c-103">Gets a route table summary of an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="48c2c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="48c2c-104">SYNTAX</span></span>

### <span data-ttu-id="48c2c-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="48c2c-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="48c2c-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="48c2c-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="48c2c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="48c2c-107">DESCRIPTION</span></span>
<span data-ttu-id="48c2c-108">Das **Cmdlet "Get-AzExpressRouteCrossConnectionRouteTableSummary"** ruft eine Zusammenfassung der BGP-Benachbarten Informationen für einen bestimmten Routingkontext ab.</span><span class="sxs-lookup"><span data-stu-id="48c2c-108">The **Get-AzExpressRouteCrossConnectionRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="48c2c-109">Diese Informationen sind hilfreich, um zu ermitteln, wie lange ein Routingkontext eingerichtet wurde und wie viele Routenpräfixe vom Peeringrouter angekündigt werden.</span><span class="sxs-lookup"><span data-stu-id="48c2c-109">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="48c2c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="48c2c-110">EXAMPLES</span></span>

### <span data-ttu-id="48c2c-111">Beispiel 1: Anzeigen der Routenzusammenfassung für den primären Pfad</span><span class="sxs-lookup"><span data-stu-id="48c2c-111">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CrossConnectionName -DevicePath 'Primary'
```

## <span data-ttu-id="48c2c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48c2c-112">PARAMETERS</span></span>

### <span data-ttu-id="48c2c-113">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="48c2c-113">-CrossConnectionName</span></span>
<span data-ttu-id="48c2c-114">Der Name der Express Route Cross Connection</span><span class="sxs-lookup"><span data-stu-id="48c2c-114">The Name of Express Route Cross Connection</span></span>

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

### <span data-ttu-id="48c2c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48c2c-115">-DefaultProfile</span></span>
<span data-ttu-id="48c2c-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="48c2c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48c2c-117">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="48c2c-117">-DevicePath</span></span>
<span data-ttu-id="48c2c-118">Die zulässigen Werte für diesen Parameter `Primary` sind: `Secondary`</span><span class="sxs-lookup"><span data-stu-id="48c2c-118">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="48c2c-119">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="48c2c-119">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="48c2c-120">Die Express Route Cross Connection</span><span class="sxs-lookup"><span data-stu-id="48c2c-120">The Express Route Cross Connection</span></span>

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

### <span data-ttu-id="48c2c-121">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="48c2c-121">-PeeringType</span></span>
<span data-ttu-id="48c2c-122">Die zulässigen Werte für diesen Parameter sind: `AzurePrivatePeering` `AzurePublicPeering` , und `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="48c2c-122">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="48c2c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48c2c-123">-ResourceGroupName</span></span>
<span data-ttu-id="48c2c-124">Der Name der Ressourcengruppe, die die ExpressRoute-Querverbindung enthält.</span><span class="sxs-lookup"><span data-stu-id="48c2c-124">The name of the resource group containing the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="48c2c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48c2c-125">CommonParameters</span></span>
<span data-ttu-id="48c2c-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48c2c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48c2c-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48c2c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48c2c-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="48c2c-128">INPUTS</span></span>

### <span data-ttu-id="48c2c-129">Keine</span><span class="sxs-lookup"><span data-stu-id="48c2c-129">None</span></span>
<span data-ttu-id="48c2c-130">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="48c2c-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="48c2c-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="48c2c-131">OUTPUTS</span></span>

### <span data-ttu-id="48c2c-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnectionRoutesTableSummary</span><span class="sxs-lookup"><span data-stu-id="48c2c-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnectionRoutesTableSummary</span></span>

## <span data-ttu-id="48c2c-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="48c2c-133">NOTES</span></span>

## <span data-ttu-id="48c2c-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="48c2c-134">RELATED LINKS</span></span>

[<span data-ttu-id="48c2c-135">Get-AzExpressRouteCrossConnectionARPTable</span><span class="sxs-lookup"><span data-stu-id="48c2c-135">Get-AzExpressRouteCrossConnectionARPTable</span></span>](Get-AzExpressRouteCrossConnectionARPTable.md)

[<span data-ttu-id="48c2c-136">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="48c2c-136">Get-AzExpressRouteCrossConnectionRouteTable</span></span>](Get-AzExpressRouteCrossConnectionRouteTable.md)
