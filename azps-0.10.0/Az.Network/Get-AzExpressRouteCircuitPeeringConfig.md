---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 47C45467-F368-4993-937E-E7E975F400B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitpeeringconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzExpressRouteCircuitPeeringConfig.md
ms.openlocfilehash: 9c52ff23d4e92af0d1f62cdfc5d5fda01b3221da
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841655"
---
# <span data-ttu-id="7d6e1-101">Get-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="7d6e1-101">Get-AzExpressRouteCircuitPeeringConfig</span></span>

## <span data-ttu-id="7d6e1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7d6e1-102">SYNOPSIS</span></span>
<span data-ttu-id="7d6e1-103">Ruft eine Express Route Circuit Peering-Konfiguration ab.</span><span class="sxs-lookup"><span data-stu-id="7d6e1-103">Gets an ExpressRoute circuit peering configuration.</span></span>

## <span data-ttu-id="7d6e1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d6e1-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitPeeringConfig [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d6e1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7d6e1-105">DESCRIPTION</span></span>
<span data-ttu-id="7d6e1-106">Das Cmdlet " **Get-AzExpressRouteCircuitPeeringConfig** " Ruft die Konfiguration einer Peering-Beziehung für einen Express Route-Schaltkreis ab.</span><span class="sxs-lookup"><span data-stu-id="7d6e1-106">The **Get-AzExpressRouteCircuitPeeringConfig** cmdlet retrieves the configuration of a peering relationship for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="7d6e1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7d6e1-107">EXAMPLES</span></span>

### <span data-ttu-id="7d6e1-108">Beispiel 1: Anzeigen der Peering-Konfiguration für einen Express Route-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="7d6e1-108">Example 1: Display the peering configuration for an ExpressRoute circuit</span></span>
```
$ckt = Get-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG
Get-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ckt
```

## <span data-ttu-id="7d6e1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d6e1-109">PARAMETERS</span></span>

### <span data-ttu-id="7d6e1-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d6e1-110">-DefaultProfile</span></span>
<span data-ttu-id="7d6e1-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7d6e1-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d6e1-112">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7d6e1-112">-ExpressRouteCircuit</span></span>
<span data-ttu-id="7d6e1-113">Das Express Route-Schaltkreis Objekt, das die Peering-Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="7d6e1-113">The ExpressRoute circuit object containing the peering configuration.</span></span>

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

### <span data-ttu-id="7d6e1-114">-Name</span><span class="sxs-lookup"><span data-stu-id="7d6e1-114">-Name</span></span>
<span data-ttu-id="7d6e1-115">Der Name der Peering-Konfiguration, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="7d6e1-115">The name of the peering configuration to be retrieved.</span></span>

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

### <span data-ttu-id="7d6e1-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d6e1-116">CommonParameters</span></span>
<span data-ttu-id="7d6e1-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d6e1-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d6e1-118">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d6e1-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d6e1-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7d6e1-119">INPUTS</span></span>

### <span data-ttu-id="7d6e1-120">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7d6e1-120">PSExpressRouteCircuit</span></span>
<span data-ttu-id="7d6e1-121">Der Parameter "ExpressRouteCircuit" akzeptiert den Wert vom Typ "PSExpressRouteCircuit" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="7d6e1-121">Parameter 'ExpressRouteCircuit' accepts value of type 'PSExpressRouteCircuit' from the pipeline</span></span>

## <span data-ttu-id="7d6e1-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7d6e1-122">OUTPUTS</span></span>

### <span data-ttu-id="7d6e1-123">Microsoft. Azure. Commands. Network. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="7d6e1-123">Microsoft.Azure.Commands.Network.Models.PSPeering</span></span>

## <span data-ttu-id="7d6e1-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="7d6e1-124">NOTES</span></span>

## <span data-ttu-id="7d6e1-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7d6e1-125">RELATED LINKS</span></span>

[<span data-ttu-id="7d6e1-126">Add-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="7d6e1-126">Add-AzExpressRouteCircuitPeeringConfig</span></span>](Add-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="7d6e1-127">Neu – AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="7d6e1-127">New-AzExpressRouteCircuitPeeringConfig</span></span>](New-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="7d6e1-128">Remove-AzExpressRouteCircuitPeeringConfig</span><span class="sxs-lookup"><span data-stu-id="7d6e1-128">Remove-AzExpressRouteCircuitPeeringConfig</span></span>](Remove-AzExpressRouteCircuitPeeringConfig.md)

[<span data-ttu-id="7d6e1-129">Satz-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7d6e1-129">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
