---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressroutecircuitpeeringconfig
schema: 2.0.0
ms.openlocfilehash: 187b7848dc3634ee67521e03f46f4684f23b9913
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848804"
---
# <span data-ttu-id="25242-101">Get-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="25242-101">Get-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="25242-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="25242-102">SYNOPSIS</span></span>
<span data-ttu-id="25242-103">Ruft eine Express Route Circuit Peering-Konfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="25242-103">Gets an ExpressRoute circuit peering configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25242-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="25242-104">SYNTAX</span></span>

```
Get-AzureRmExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25242-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="25242-105">DESCRIPTION</span></span>
<span data-ttu-id="25242-106">Das Cmdlet " **Get-AzureRmExpressRouteCircuitPeeringConfig** " Ruft die Konfiguration einer Peering-Beziehung für einen Express Route-Schaltkreis ab.</span><span class="sxs-lookup"><span data-stu-id="25242-106">The **Get-AzureRmExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="25242-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="25242-107">EXAMPLES</span></span>

### <span data-ttu-id="25242-108">Beispiel 1: Anzeigen der Peering-Konfiguration für einen Express Route-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="25242-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzureRmExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="25242-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="25242-109">PARAMETERS</span></span>

### <span data-ttu-id="25242-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25242-110">-DefaultProfile</span></span>
<span data-ttu-id="25242-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="25242-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25242-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="25242-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="25242-113">Das Express Route-Schaltkreis Objekt, das die Peering-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="25242-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

```yaml
Type: PSExpressRouteCircuit
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25242-114">-Name</span><span class="sxs-lookup"><span data-stu-id="25242-114">-Name</span></span>
<span data-ttu-id="25242-115">Der Name der Peering-Konfiguration, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="25242-115">The name of the peering configuration to be retrieved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25242-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25242-116">CommonParameters</span></span>
<span data-ttu-id="25242-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25242-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25242-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25242-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25242-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="25242-119">INPUTS</span></span>

### <span data-ttu-id="25242-120">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="25242-120">PSExpressRouteCircuit</span></span>
<span data-ttu-id="25242-121">Der Parameter "ExpressRouteCircuit" akzeptiert den Wert vom Typ "PSExpressRouteCircuit" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="25242-121">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="25242-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="25242-122">OUTPUTS</span></span>

### <span data-ttu-id="25242-123">Microsoft. Azure. Commands. Network. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="25242-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="25242-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="25242-124">NOTES</span></span>

## <span data-ttu-id="25242-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="25242-125">RELATED LINKS</span></span>

[<span data-ttu-id="25242-126">Add-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="25242-126">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="25242-127">Neu – AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="25242-127">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="25242-128">Remove-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="25242-128">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Remove-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="25242-129">Satz-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="25242-129">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
