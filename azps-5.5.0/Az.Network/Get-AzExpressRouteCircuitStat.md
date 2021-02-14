---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CFE184E2-6DEF-4E92-A9C3-E82F29BB4FB8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitstat
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitStat.md
ms.openlocfilehash: 15b02ce4693e452bda370c9fb1ae9c69012e9574
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100154452"
---
# <span data-ttu-id="6241a-101">Get-AzExpressRouteCircuitStat</span><span class="sxs-lookup"><span data-stu-id="6241a-101">Get-AzExpressRouteCircuitStat</span></span>

## <span data-ttu-id="6241a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6241a-102">SYNOPSIS</span></span>
<span data-ttu-id="6241a-103">Ruft Nutzungsstatistiken für einen "ExpressRoute"-Schaltkreis ab.</span><span class="sxs-lookup"><span data-stu-id="6241a-103">Gets usage statistics of an ExpressRoute circuit.</span></span>

## <span data-ttu-id="6241a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6241a-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitStat -ResourceGroupName <String> -ExpressRouteCircuitName <String>
 [-PeeringType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6241a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6241a-105">DESCRIPTION</span></span>
<span data-ttu-id="6241a-106">Das **Cmdlet "Get-AzExpressRouteCircuitStat"** ruft Verkehrsstatistiken für einen "ExpressRoute"-Schaltkreis ab.</span><span class="sxs-lookup"><span data-stu-id="6241a-106">The **Get-AzExpressRouteCircuitStat** cmdlet retrieves traffic statistics for an ExpressRoute circuit.</span></span> <span data-ttu-id="6241a-107">Die Statistiken umfassen die Anzahl der gesendeten und empfangenen Bytes über die primären und sekundären Routen.</span><span class="sxs-lookup"><span data-stu-id="6241a-107">The statistics include the number of bytes sent and received over both the primary and secondary routes.</span></span>

## <span data-ttu-id="6241a-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6241a-108">EXAMPLES</span></span>

### <span data-ttu-id="6241a-109">Beispiel 1: Anzeigen der Verkehrsstatistiken für einen ExpressRoute-Peer</span><span class="sxs-lookup"><span data-stu-id="6241a-109">Example 1: Display the traffic statistics for an ExpressRoute peer</span></span>
```
Get-AzExpressRouteCircuitStat -ResourceGroupName $RG -ExpressRouteCircuitName $CircuitName -PeeringType 'AzurePrivatePeering'
```

## <span data-ttu-id="6241a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6241a-110">PARAMETERS</span></span>

### <span data-ttu-id="6241a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6241a-111">-DefaultProfile</span></span>
<span data-ttu-id="6241a-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6241a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6241a-113">-ExpressRouteCircuitName</span><span class="sxs-lookup"><span data-stu-id="6241a-113">-ExpressRouteCircuitName</span></span>
<span data-ttu-id="6241a-114">Der Name des zu untersuchende ExpressRoute-Schaltkreises.</span><span class="sxs-lookup"><span data-stu-id="6241a-114">The name of the ExpressRoute circuit being examined.</span></span>

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

### <span data-ttu-id="6241a-115">-PeeringType</span><span class="sxs-lookup"><span data-stu-id="6241a-115">-PeeringType</span></span>
<span data-ttu-id="6241a-116">Die zulässigen Werte für diesen Parameter sind: `AzurePrivatePeering` `AzurePublicPeering` , und `MicrosoftPeering`</span><span class="sxs-lookup"><span data-stu-id="6241a-116">The acceptable values for this parameter are: `AzurePrivatePeering`, `AzurePublicPeering`, and `MicrosoftPeering`</span></span>

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

### <span data-ttu-id="6241a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6241a-117">-ResourceGroupName</span></span>
<span data-ttu-id="6241a-118">Der Name der Ressourcengruppe, die den "ExpressRoute"-Schaltkreis enthält.</span><span class="sxs-lookup"><span data-stu-id="6241a-118">The name of the resource group containing the ExpressRoute circuit.</span></span>

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

### <span data-ttu-id="6241a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6241a-119">CommonParameters</span></span>
<span data-ttu-id="6241a-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6241a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6241a-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6241a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6241a-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6241a-122">INPUTS</span></span>

### <span data-ttu-id="6241a-123">System.String</span><span class="sxs-lookup"><span data-stu-id="6241a-123">System.String</span></span>

## <span data-ttu-id="6241a-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6241a-124">OUTPUTS</span></span>

### <span data-ttu-id="6241a-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span><span class="sxs-lookup"><span data-stu-id="6241a-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitStats</span></span>

## <span data-ttu-id="6241a-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6241a-126">NOTES</span></span>

## <span data-ttu-id="6241a-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6241a-127">RELATED LINKS</span></span>

[<span data-ttu-id="6241a-128">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="6241a-128">Get-AzExpressRouteCircuitARPTable</span></span>](Get-AzExpressRouteCircuitARPTable.md)

[<span data-ttu-id="6241a-129">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="6241a-129">Get-AzExpressRouteCircuitRouteTable</span></span>](Get-AzExpressRouteCircuitRouteTable.md)

[<span data-ttu-id="6241a-130">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="6241a-130">Get-AzExpressRouteCircuitRouteTableSummary</span></span>](Get-AzExpressRouteCircuitRouteTableSummary.md)
