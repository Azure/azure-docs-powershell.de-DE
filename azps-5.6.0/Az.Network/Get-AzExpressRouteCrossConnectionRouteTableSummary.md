---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C603E0E-A19F-4EA6-B918-945007BE22FF
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecrossconnectionroutetablesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTableSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnectionRouteTableSummary.md
ms.openlocfilehash: d5b6d1b9e5d3955b7ecbff9dec02405e030bbf33
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932411"
---
# <span data-ttu-id="ea1e3-101">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ea1e3-101">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

## <span data-ttu-id="ea1e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea1e3-102">SYNOPSIS</span></span>
<span data-ttu-id="ea1e3-103">Ruft eine Zusammenfassung einer ExpressRoute-Querverbindung ab.</span><span class="sxs-lookup"><span data-stu-id="ea1e3-103">Gets a route table summary of an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="ea1e3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ea1e3-104">SYNTAX</span></span>

### <span data-ttu-id="ea1e3-105">SpecifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="ea1e3-105">SpecifyByParameterValues</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ResourceGroupName <String> -CrossConnectionName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ea1e3-106">SpecifyByReference</span><span class="sxs-lookup"><span data-stu-id="ea1e3-106">SpecifyByReference</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ea1e3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ea1e3-107">DESCRIPTION</span></span>
<span data-ttu-id="ea1e3-108">Das **Get-AzExpressRouteCrossConnectionRouteTableSummary-Cmdlet** ruft eine Zusammenfassung der BGP-Nachbarinformationen für einen bestimmten Routingkontext ab.</span><span class="sxs-lookup"><span data-stu-id="ea1e3-108">The **Get-AzExpressRouteCrossConnectionRouteTableSummary** cmdlet retrieves a summary of BGP neighbor information for a particular routing context.</span></span> <span data-ttu-id="ea1e3-109">Diese Informationen sind hilfreich, um zu ermitteln, wie lange ein Routingkontext eingerichtet wurde und wie viele Routenpräfixe vom Peeringrouter angekündigt wurden.</span><span class="sxs-lookup"><span data-stu-id="ea1e3-109">This information is useful to determine for how long a routing context has been established and the number of route prefixes advertised by the peering router.</span></span>

## <span data-ttu-id="ea1e3-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ea1e3-110">EXAMPLES</span></span>

### <span data-ttu-id="ea1e3-111">Beispiel 1: Anzeigen der Routenzusammenfassung für den primären Pfad</span><span class="sxs-lookup"><span data-stu-id="ea1e3-111">Example 1: Display the route summary for the primary path</span></span>
```
Get-AzExpressRouteCrossConnectionRouteTableSummary -ResourceGroupName $RG -ExpressRouteCrossConnectionName $CrossConnectionName -DevicePath 'Primary'
```

## <span data-ttu-id="ea1e3-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ea1e3-112">PARAMETERS</span></span>

### <span data-ttu-id="ea1e3-113">-CrossConnectionName</span><span class="sxs-lookup"><span data-stu-id="ea1e3-113">-CrossConnectionName</span></span>
<span data-ttu-id="ea1e3-114">Der Name der ExpressRoute Cross Connection</span><span class="sxs-lookup"><span data-stu-id="ea1e3-114">The Name of Express Route Cross Connection</span></span>

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

### <span data-ttu-id="ea1e3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea1e3-115">-DefaultProfile</span></span>
<span data-ttu-id="ea1e3-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ea1e3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea1e3-117">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="ea1e3-117">-DevicePath</span></span>
<span data-ttu-id="ea1e3-118">Die zulässigen Werte für diesen Parameter sind: `Primary` oder `Secondary`</span><span class="sxs-lookup"><span data-stu-id="ea1e3-118">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="ea1e3-119">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ea1e3-119">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="ea1e3-120">Die Expressroutenkreuzverbindung</span><span class="sxs-lookup"><span data-stu-id="ea1e3-120">The Express Route Cross Connection</span></span>

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

### <span data-ttu-id="ea1e3-121">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="ea1e3-121">-PeeringType</span></span>
<span data-ttu-id="ea1e3-122">Die zulässigen Werte für diesen Parameter sind: `AzurePrivatePeering` `AzurePublicPeering` , und `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="ea1e3-122">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="ea1e3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea1e3-123">-ResourceGroupName</span></span>
<span data-ttu-id="ea1e3-124">Der Name der Ressourcengruppe, die die ExpressRoute-Querverbindung enthält.</span><span class="sxs-lookup"><span data-stu-id="ea1e3-124">The name of the resource group containing the ExpressRoute cross connection.</span></span>

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

### <span data-ttu-id="ea1e3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea1e3-125">CommonParameters</span></span>
<span data-ttu-id="ea1e3-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea1e3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea1e3-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ea1e3-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea1e3-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ea1e3-128">INPUTS</span></span>

### <span data-ttu-id="ea1e3-129">Keine</span><span class="sxs-lookup"><span data-stu-id="ea1e3-129">None</span></span>
<span data-ttu-id="ea1e3-130">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="ea1e3-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ea1e3-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ea1e3-131">OUTPUTS</span></span>

### <span data-ttu-id="ea1e3-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnectionRoutesTableSummary</span><span class="sxs-lookup"><span data-stu-id="ea1e3-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnectionRoutesTableSummary</span></span>

## <span data-ttu-id="ea1e3-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ea1e3-133">NOTES</span></span>

## <span data-ttu-id="ea1e3-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ea1e3-134">RELATED LINKS</span></span>

[<span data-ttu-id="ea1e3-135">Get-AzExpressRouteCrossConnectionARPTable</span><span class="sxs-lookup"><span data-stu-id="ea1e3-135">Get-AzExpressRouteCrossConnectionARPTable</span></span>](Get-AzExpressRouteCrossConnectionARPTable.md)

[<span data-ttu-id="ea1e3-136">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="ea1e3-136">Get-AzExpressRouteCrossConnectionRouteTable</span></span>](Get-AzExpressRouteCrossConnectionRouteTable.md)
