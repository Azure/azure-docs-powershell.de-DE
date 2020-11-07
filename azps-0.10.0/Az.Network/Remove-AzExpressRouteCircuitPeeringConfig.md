---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 5feeba4ffb4f73365e9b6df86a03e8920b74f88e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841156"
---
# <span data-ttu-id="0c64d-101">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="0c64d-101">Remove-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="0c64d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0c64d-102">SYNOPSIS</span></span>
<span data-ttu-id="0c64d-103">Entfernt eine Express Route Circuit-Peering-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="0c64d-103">Removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="0c64d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c64d-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-PeerAddressType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c64d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0c64d-105">DESCRIPTION</span></span>
<span data-ttu-id="0c64d-106">Das Cmdlet " **Remove-AzExpressRouteCircuitPeeringConfig** " entfernt eine Express Route Circuit-Peering-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="0c64d-106">The **Remove-AzExpressRouteCircuitPeeringConfig** cmdlet removes an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="0c64d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0c64d-107">EXAMPLES</span></span>

### <span data-ttu-id="0c64d-108">Beispiel 1: Entfernen einer Peering-Konfiguration von einem Express Route-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="0c64d-108">Example 1: Remove a peering configuration from an ExpressRoute circuit</span></span>
```
$circuit = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitPeeringConfig -Name 'AzurePrivatePeering' -ExpressRouteCircuit $circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit
```

## <span data-ttu-id="0c64d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c64d-109">PARAMETERS</span></span>

### <span data-ttu-id="0c64d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c64d-110">-DefaultProfile</span></span>
<span data-ttu-id="0c64d-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0c64d-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c64d-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0c64d-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="0c64d-113">Der Express Route-Schaltkreis mit der Peering-Konfiguration, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0c64d-113">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="0c64d-114">-Name</span><span class="sxs-lookup"><span data-stu-id="0c64d-114">-Name</span></span>
<span data-ttu-id="0c64d-115">Der Name der zu entfernende Peering-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="0c64d-115">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="0c64d-116">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="0c64d-116">-PeerAddressType</span></span>
<span data-ttu-id="0c64d-117">Die Adressfamilie des Peerings</span><span class="sxs-lookup"><span data-stu-id="0c64d-117">The Address family of the peering</span></span>

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

### <span data-ttu-id="0c64d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c64d-118">CommonParameters</span></span>
<span data-ttu-id="0c64d-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c64d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c64d-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c64d-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c64d-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0c64d-121">INPUTS</span></span>

### <span data-ttu-id="0c64d-122">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0c64d-122">PSExpressRouteCircuit</span></span>
<span data-ttu-id="0c64d-123">Der Parameter "ExpressRouteCircuit" akzeptiert den Wert vom Typ "PSExpressRouteCircuit" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="0c64d-123">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="0c64d-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0c64d-124">OUTPUTS</span></span>

### <span data-ttu-id="0c64d-125">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0c64d-125">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="0c64d-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="0c64d-126">NOTES</span></span>

## <span data-ttu-id="0c64d-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0c64d-127">RELATED LINKS</span></span>

[<span data-ttu-id="0c64d-128">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="0c64d-128">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="0c64d-129">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0c64d-129">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="0c64d-130">Neu – AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="0c64d-130">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="0c64d-131">Satz-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0c64d-131">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
