---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermexpressroutecircuitpeeringconfig
schema: 2.0.0
ms.openlocfilehash: 749f1b84ed033e903d3e50652e6199f184fffa2b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848724"
---
# <span data-ttu-id="4c2cb-101">Remove-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="4c2cb-101">Remove-AzureRmExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="4c2cb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4c2cb-102">SYNOPSIS</span></span>
<span data-ttu-id="4c2cb-103">Entfernt eine Express Route Circuit-Peering-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="4c2cb-103">Removes an ExpressRoute circuit peering configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c2cb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c2cb-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c2cb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4c2cb-105">DESCRIPTION</span></span>
<span data-ttu-id="4c2cb-106">Das Cmdlet " **Remove-AzureRmExpressRouteCircuitPeeringConfig** " entfernt eine Express Route Circuit-Peering-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="4c2cb-106">The **Remove-AzureRmExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="4c2cb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4c2cb-107">EXAMPLES</span></span>

### <span data-ttu-id="4c2cb-108">Beispiel 1: Entfernen einer Peering-Konfiguration von einem Express Route-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="4c2cb-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzureRmExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzureRmExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="4c2cb-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4c2cb-109">PARAMETERS</span></span>

### <span data-ttu-id="4c2cb-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c2cb-110">-DefaultProfile</span></span>
<span data-ttu-id="4c2cb-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4c2cb-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c2cb-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4c2cb-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="4c2cb-113">Der Express Route-Schaltkreis mit der Peering-Konfiguration, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4c2cb-113">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="4c2cb-114">-Name</span><span class="sxs-lookup"><span data-stu-id="4c2cb-114">-Name</span></span>
<span data-ttu-id="4c2cb-115">Der Name der zu entfernende Peering-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="4c2cb-115">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="4c2cb-116">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="4c2cb-116">-PeerAddressType</span></span>
<span data-ttu-id="4c2cb-117">Die Adressfamilie des Peerings</span><span class="sxs-lookup"><span data-stu-id="4c2cb-117">The Address family of the peering</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c2cb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c2cb-118">CommonParameters</span></span>
<span data-ttu-id="4c2cb-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c2cb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c2cb-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c2cb-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c2cb-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4c2cb-121">INPUTS</span></span>

### <span data-ttu-id="4c2cb-122">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4c2cb-122">PSExpressRouteCircuit</span></span>
<span data-ttu-id="4c2cb-123">Der Parameter "ExpressRouteCircuit" akzeptiert den Wert vom Typ "PSExpressRouteCircuit" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="4c2cb-123">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="4c2cb-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4c2cb-124">OUTPUTS</span></span>

### <span data-ttu-id="4c2cb-125">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4c2cb-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="4c2cb-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="4c2cb-126">NOTES</span></span>

## <span data-ttu-id="4c2cb-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4c2cb-127">RELATED LINKS</span></span>

[<span data-ttu-id="4c2cb-128">Add-AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="4c2cb-128">Add-AzureRmExpressRouteCircuitPeeringConfig</span></span>](Add-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="4c2cb-129">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4c2cb-129">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="4c2cb-130">Neu – AzureRmExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="4c2cb-130">New-AzureRmExpressRouteCircuitPeeringConfig</span></span>](New-AzureRmExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="4c2cb-131">Satz-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="4c2cb-131">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
