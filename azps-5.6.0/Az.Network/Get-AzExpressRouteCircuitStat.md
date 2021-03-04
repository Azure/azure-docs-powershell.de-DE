---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CFE184E2-6DEF-4E92-A9C3-E82F29BB4FB8
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecircuitstat
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
ms.openlocfilehash: e0f4b24581860f17024c9b01e62b3c84616c6f81
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942435"
---
# <span data-ttu-id="86349-101">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="86349-101">Get-AzExpressRouteCircuitStat</span></span>

## <span data-ttu-id="86349-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86349-102">SYNOPSIS</span></span>
<span data-ttu-id="86349-103">Ruft Nutzungsstatistiken eines ExpressRoute-Schaltkreises ab.</span><span class="sxs-lookup"><span data-stu-id="86349-103">Gets usage statistics of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="86349-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="86349-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitStat -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86349-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="86349-105">DESCRIPTION</span></span>
<span data-ttu-id="86349-106">Das **Get-AzExpressRouteCircuitStat-Cmdlet** ruft Verkehrsstatistiken für einen ExpressRoute-Schaltkreis ab.</span><span class="sxs-lookup"><span data-stu-id="86349-106">The **Get-AzExpressRouteCircuitStat** cmdlet retrieves traffic statistics for an ExpressRoute circuit.</span></span> <span data-ttu-id="86349-107">Die Statistik enthält die Anzahl der bytes, die über die primären und sekundären Routen gesendet und empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="86349-107">The statistics include the number of bytes sent and received over both the primary and secondary routes.</span></span>

## <span data-ttu-id="86349-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="86349-108">EXAMPLES</span></span>

### <span data-ttu-id="86349-109">Beispiel 1: Anzeigen der Verkehrsstatistiken für einen ExpressRoute-Peer</span><span class="sxs-lookup"><span data-stu-id="86349-109">Example 1: Display the traffic statistics for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitStat -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType 'AzurePrivatePeering'
```

## <span data-ttu-id="86349-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="86349-110">PARAMETERS</span></span>

### <span data-ttu-id="86349-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86349-111">-DefaultProfile</span></span>
<span data-ttu-id="86349-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="86349-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86349-113">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="86349-113">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="86349-114">Der Name des zu untersuchende ExpressRoute-Schaltkreises.</span><span class="sxs-lookup"><span data-stu-id="86349-114">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="86349-115">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="86349-115">-PeeringType</span></span>
<span data-ttu-id="86349-116">Die zulässigen Werte für diesen Parameter sind: `AzurePrivatePeering` `AzurePublicPeering` , und `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="86349-116">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzurePrivatePeering, AzurePublicPeering, MicrosoftPeering

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86349-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86349-117">-ResourceGroupName</span></span>
<span data-ttu-id="86349-118">Der Name der Ressourcengruppe, die den ExpressRoute-Schaltkreis enthält.</span><span class="sxs-lookup"><span data-stu-id="86349-118">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="86349-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86349-119">CommonParameters</span></span>
<span data-ttu-id="86349-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86349-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86349-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="86349-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86349-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="86349-122">INPUTS</span></span>

### <span data-ttu-id="86349-123">System.String</span><span class="sxs-lookup"><span data-stu-id="86349-123">System.String</span></span>

## <span data-ttu-id="86349-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="86349-124">OUTPUTS</span></span>

### <span data-ttu-id="86349-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="86349-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span></span>

## <span data-ttu-id="86349-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="86349-126">NOTES</span></span>

## <span data-ttu-id="86349-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="86349-127">RELATED LINKS</span></span>

[<span data-ttu-id="86349-128">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="86349-128">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="86349-129">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="86349-129">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="86349-130">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="86349-130">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)
