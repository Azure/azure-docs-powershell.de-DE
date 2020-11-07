---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: c8e821408f3d65ace31ab2340f544a0a47e120e6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660805"
---
# <span data-ttu-id="1c70f-101">Get-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="1c70f-101">Get-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="1c70f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1c70f-102">SYNOPSIS</span></span>
<span data-ttu-id="1c70f-103">Ruft eine Express Route Circuit Peering-Konfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="1c70f-103">Gets an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="1c70f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c70f-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c70f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1c70f-105">DESCRIPTION</span></span>
<span data-ttu-id="1c70f-106">Das Cmdlet " **Get-AzExpressRouteCircuitPeeringConfig** " Ruft die Konfiguration einer Peering-Beziehung für einen Express Route-Schaltkreis ab.</span><span class="sxs-lookup"><span data-stu-id="1c70f-106">The **Get-AzExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="1c70f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1c70f-107">EXAMPLES</span></span>

### <span data-ttu-id="1c70f-108">Beispiel 1: Anzeigen der Peering-Konfiguration für einen Express Route-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="1c70f-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="1c70f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1c70f-109">PARAMETERS</span></span>

### <span data-ttu-id="1c70f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c70f-110">-DefaultProfile</span></span>
<span data-ttu-id="1c70f-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1c70f-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c70f-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1c70f-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="1c70f-113">Das Express Route-Schaltkreis Objekt, das die Peering-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="1c70f-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c70f-114">-Name</span><span class="sxs-lookup"><span data-stu-id="1c70f-114">-Name</span></span>
<span data-ttu-id="1c70f-115">Der Name der Peering-Konfiguration, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="1c70f-115">The name of the peering configuration to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c70f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c70f-116">CommonParameters</span></span>
<span data-ttu-id="1c70f-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c70f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c70f-118">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c70f-118">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c70f-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1c70f-119">INPUTS</span></span>

### <span data-ttu-id="1c70f-120">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1c70f-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="1c70f-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1c70f-121">OUTPUTS</span></span>

### <span data-ttu-id="1c70f-122">Microsoft. Azure. Commands. Network. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="1c70f-122">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="1c70f-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="1c70f-123">NOTES</span></span>

## <span data-ttu-id="1c70f-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1c70f-124">RELATED LINKS</span></span>

[<span data-ttu-id="1c70f-125">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="1c70f-125">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="1c70f-126">Neu – AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="1c70f-126">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="1c70f-127">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="1c70f-127">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="1c70f-128">Satz-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="1c70f-128">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
