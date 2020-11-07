---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: c7d60c3d2f69e7ea18bcd256d8ad4a943817769a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660386"
---
# <span data-ttu-id="a43da-101">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="a43da-101">Remove-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="a43da-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a43da-102">SYNOPSIS</span></span>
<span data-ttu-id="a43da-103">Entfernt eine Express Route Circuit-Peering-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="a43da-103">Removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="a43da-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a43da-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a43da-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a43da-105">DESCRIPTION</span></span>
<span data-ttu-id="a43da-106">Das Cmdlet " **Remove-AzExpressRouteCircuitPeeringConfig** " entfernt eine Express Route Circuit-Peering-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="a43da-106">The **Remove-AzExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="a43da-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a43da-107">EXAMPLES</span></span>

### <span data-ttu-id="a43da-108">Beispiel 1: Entfernen einer Peering-Konfiguration von einem Express Route-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="a43da-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="a43da-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a43da-109">PARAMETERS</span></span>

### <span data-ttu-id="a43da-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a43da-110">-DefaultProfile</span></span>
<span data-ttu-id="a43da-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a43da-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a43da-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a43da-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="a43da-113">Der Express Route-Schaltkreis mit der Peering-Konfiguration, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a43da-113">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="a43da-114">-Name</span><span class="sxs-lookup"><span data-stu-id="a43da-114">-Name</span></span>
<span data-ttu-id="a43da-115">Der Name der zu entfernende Peering-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="a43da-115">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="a43da-116">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="a43da-116">-PeerAddressType</span></span>
<span data-ttu-id="a43da-117">Die Adressfamilie des Peerings</span><span class="sxs-lookup"><span data-stu-id="a43da-117">The Address family of the peering</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a43da-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a43da-118">CommonParameters</span></span>
<span data-ttu-id="a43da-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a43da-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a43da-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a43da-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a43da-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a43da-121">INPUTS</span></span>

### <span data-ttu-id="a43da-122">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a43da-122">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="a43da-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a43da-123">OUTPUTS</span></span>

### <span data-ttu-id="a43da-124">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a43da-124">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="a43da-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="a43da-125">NOTES</span></span>

## <span data-ttu-id="a43da-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a43da-126">RELATED LINKS</span></span>

[<span data-ttu-id="a43da-127">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="a43da-127">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="a43da-128">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a43da-128">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="a43da-129">Neu – AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="a43da-129">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="a43da-130">Satz-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a43da-130">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
