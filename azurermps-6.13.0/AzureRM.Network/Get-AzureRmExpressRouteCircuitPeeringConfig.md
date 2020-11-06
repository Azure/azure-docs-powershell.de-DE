---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 204d70753d3a4ae80e05dfff90d4a5b50b47ab58
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504365"
---
# <span data-ttu-id="f8ae4-101">Get-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="f8ae4-101">Get-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="f8ae4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f8ae4-102">SYNOPSIS</span></span>
<span data-ttu-id="f8ae4-103">Ruft eine Express Route Circuit Peering-Konfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="f8ae4-103">Gets an ExpressRoute circuit peering configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8ae4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8ae4-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f8ae4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f8ae4-105">DESCRIPTION</span></span>
<span data-ttu-id="f8ae4-106">Das Cmdlet " **Get-AzureRmExpressRouteCircuitPeeringConfig** " Ruft die Konfiguration einer Peering-Beziehung für einen Express Route-Schaltkreis ab.</span><span class="sxs-lookup"><span data-stu-id="f8ae4-106">The **Get-AzureRmExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="f8ae4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f8ae4-107">EXAMPLES</span></span>

### <span data-ttu-id="f8ae4-108">Beispiel 1: Anzeigen der Peering-Konfiguration für einen Express Route-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="f8ae4-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzureRmExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="f8ae4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8ae4-109">PARAMETERS</span></span>

### <span data-ttu-id="f8ae4-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8ae4-110">-DefaultProfile</span></span>
<span data-ttu-id="f8ae4-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f8ae4-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8ae4-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f8ae4-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="f8ae4-113">Das Express Route-Schaltkreis Objekt, das die Peering-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="f8ae4-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

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

### <span data-ttu-id="f8ae4-114">-Name</span><span class="sxs-lookup"><span data-stu-id="f8ae4-114">-Name</span></span>
<span data-ttu-id="f8ae4-115">Der Name der Peering-Konfiguration, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f8ae4-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="f8ae4-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8ae4-116">CommonParameters</span></span>
<span data-ttu-id="f8ae4-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8ae4-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8ae4-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8ae4-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8ae4-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f8ae4-119">INPUTS</span></span>

### <span data-ttu-id="f8ae4-120">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f8ae4-120">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>
<span data-ttu-id="f8ae4-121">Parameter: ExpressRouteCircuit (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f8ae4-121">Parameters: ExpressRouteCircuit (ByValue)</span></span>

## <span data-ttu-id="f8ae4-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f8ae4-122">OUTPUTS</span></span>

### <span data-ttu-id="f8ae4-123">Microsoft. Azure. Commands. Network. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="f8ae4-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="f8ae4-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="f8ae4-124">NOTES</span></span>

## <span data-ttu-id="f8ae4-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f8ae4-125">RELATED LINKS</span></span>

[<span data-ttu-id="f8ae4-126">Add-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="f8ae4-126">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="f8ae4-127">Neu – AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="f8ae4-127">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="f8ae4-128">Remove-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="f8ae4-128">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="f8ae4-129">Satz-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="f8ae4-129">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
