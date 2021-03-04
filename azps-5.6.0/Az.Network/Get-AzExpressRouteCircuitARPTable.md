---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F0370845-13D9-4FB5-B30E-826A22EBC5E0
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecircuitarptable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitARPTable.md
ms.openlocfilehash: b82ef556db076c46fbfe098ba2c2f76e9abab862
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926544"
---
# <span data-ttu-id="c17c5-101">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="c17c5-101">Get-AzExpressRouteCircuitARPTable</span></span>

## <span data-ttu-id="c17c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c17c5-102">SYNOPSIS</span></span>
<span data-ttu-id="c17c5-103">Ruft die ARP-Tabelle aus einem ExpressRoute-Schaltkreis ab.</span><span class="sxs-lookup"><span data-stu-id="c17c5-103">Gets the ARP table from an ExpressRoute circuit.</span></span>

## <span data-ttu-id="c17c5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c17c5-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 -PeeringType <String> -DevicePath <DevicePathEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c17c5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c17c5-105">DESCRIPTION</span></span>
<span data-ttu-id="c17c5-106">Das **Get-AzExpressRouteCircuitARPTable-Cmdlet** ruft die ARP-Tabelle aus beiden Schnittstellen eines ExpressRoute-Schaltkreises ab.</span><span class="sxs-lookup"><span data-stu-id="c17c5-106">The **Get-AzExpressRouteCircuitARPTable** cmdlet retrieves the ARP table from both interfaces of an ExpressRoute circuit.</span></span> <span data-ttu-id="c17c5-107">Die TABELLE ARP enthält eine Zuordnung der IPv4-Adresse zu der MAC-Adresse für ein bestimmtes Peering.</span><span class="sxs-lookup"><span data-stu-id="c17c5-107">The ARP table provides a mapping of the IPv4 address to MAC address for a particular peering.</span></span> <span data-ttu-id="c17c5-108">Sie können die ARP-Tabelle verwenden, um die Konfiguration und Konnektivität der Ebene 2 zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="c17c5-108">You can use the ARP table to validate layer 2 configuration and connectivity.</span></span>

## <span data-ttu-id="c17c5-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c17c5-109">EXAMPLES</span></span>

### <span data-ttu-id="c17c5-110">Beispiel 1: Anzeigen der ARP-Tabelle für einen ExpressRoute-Peer</span><span class="sxs-lookup"><span data-stu-id="c17c5-110">Example 1: Display the ARP table for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitARPTable -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType MicrosoftPeering -DevicePath Primary
```

## <span data-ttu-id="c17c5-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c17c5-111">PARAMETERS</span></span>

### <span data-ttu-id="c17c5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c17c5-112">-DefaultProfile</span></span>
<span data-ttu-id="c17c5-113">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c17c5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c17c5-114">-DevicePath</span><span class="sxs-lookup"><span data-stu-id="c17c5-114">-DevicePath</span></span>
<span data-ttu-id="c17c5-115">Die zulässigen Werte für diesen Parameter sind: `Primary` oder `Secondary`</span><span class="sxs-lookup"><span data-stu-id="c17c5-115">The acceptable values for this parameter are: `Primary` or `Secondary`</span></span>

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

### <span data-ttu-id="c17c5-116">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="c17c5-116">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="c17c5-117">Der Name des zu untersuchende ExpressRoute-Schaltkreises.</span><span class="sxs-lookup"><span data-stu-id="c17c5-117">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="c17c5-118">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="c17c5-118">-PeeringType</span></span>
<span data-ttu-id="c17c5-119">Die zulässigen Werte für diesen Parameter sind: `AzurePrivatePeering` `AzurePublicPeering` , und `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="c17c5-119">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="c17c5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c17c5-120">-ResourceGroupName</span></span>
<span data-ttu-id="c17c5-121">Der Name der Ressourcengruppe, die den ExpressRoute-Schaltkreis enthält.</span><span class="sxs-lookup"><span data-stu-id="c17c5-121">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="c17c5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c17c5-122">CommonParameters</span></span>
<span data-ttu-id="c17c5-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c17c5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c17c5-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c17c5-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c17c5-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c17c5-125">INPUTS</span></span>

### <span data-ttu-id="c17c5-126">System.String</span><span class="sxs-lookup"><span data-stu-id="c17c5-126">System.String</span></span>

## <span data-ttu-id="c17c5-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c17c5-127">OUTPUTS</span></span>

### <span data-ttu-id="c17c5-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span><span class="sxs-lookup"><span data-stu-id="c17c5-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitArpTable</span></span>

## <span data-ttu-id="c17c5-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c17c5-129">NOTES</span></span>

## <span data-ttu-id="c17c5-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c17c5-130">RELATED LINKS</span></span>

[<span data-ttu-id="c17c5-131">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="c17c5-131">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="c17c5-132">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="c17c5-132">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)

[<span data-ttu-id="c17c5-133">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="c17c5-133">Get-AzExpressRouteCircuitStat</span></span>](./Get-AzExpressRouteCircuitStat.md)
