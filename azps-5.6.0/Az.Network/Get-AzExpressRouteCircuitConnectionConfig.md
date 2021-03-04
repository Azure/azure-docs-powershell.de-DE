---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59692f1f-9f1e-4a3c-8200-312c3806a9b7
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: c8d35373c2891b9f0d3ac76ded8b4e9808f32f33
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940200"
---
# <span data-ttu-id="063bf-101">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="063bf-101">Get-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="063bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="063bf-102">SYNOPSIS</span></span>
<span data-ttu-id="063bf-103">Ruft eine ExpressRoute-Verbindungskonfiguration ab, die mit privatem Peering von ExpressRouteCircuit verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="063bf-103">Gets an ExpressRoute circuit connection configuration associated with Private Peering of ExpressRouteCircuit.</span></span>

## <span data-ttu-id="063bf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="063bf-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitConnectionConfig [[-Name] <String>] [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="063bf-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="063bf-105">DESCRIPTION</span></span>
<span data-ttu-id="063bf-106">Das **Get-AzExpressRouteCircuitConnectionConfig-Cmdlet** ruft die Konfiguration einer Schaltungsverbindung ab, die privatem Peering für einen ExpressRoute-Schaltkreis zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="063bf-106">The **Get-AzExpressRouteCircuitConnectionConfig** cmdlet retrieves the configuration of a circuit connection associated with Private Peering for an ExpressRoute circuit.</span></span>

## <span data-ttu-id="063bf-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="063bf-107">EXAMPLES</span></span>

### <span data-ttu-id="063bf-108">Beispiel 1: Anzeigen der Verbindungskonfiguration für einen ExpressRoute-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="063bf-108">Example 1: Display the circuit connection configuration for an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="063bf-109">Beispiel 2: Erhalten einer Mit einem ExpressRoute-Schaltkreis zugeordneten Verbindungsressource mithilfe von Piping</span><span class="sxs-lookup"><span data-stu-id="063bf-109">Example 2: Get circuit connection resource associated with an ExpressRoute Circuit using piping</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Get-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName
```

## <span data-ttu-id="063bf-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="063bf-110">PARAMETERS</span></span>

### <span data-ttu-id="063bf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="063bf-111">-DefaultProfile</span></span>
<span data-ttu-id="063bf-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="063bf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="063bf-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="063bf-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="063bf-114">Das ExpressRoute-Schaltkreisobjekt, das die Verbindungskonfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="063bf-114">The ExpressRoute circuit object containing the circuit connection configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="063bf-115">-Name</span><span class="sxs-lookup"><span data-stu-id="063bf-115">-Name</span></span>
<span data-ttu-id="063bf-116">Der Name der Verbindungskonfiguration, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="063bf-116">The name of the circuit connection configuration to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="063bf-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="063bf-117">CommonParameters</span></span>
<span data-ttu-id="063bf-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="063bf-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="063bf-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="063bf-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="063bf-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="063bf-120">INPUTS</span></span>

### <span data-ttu-id="063bf-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="063bf-121">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="063bf-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="063bf-122">OUTPUTS</span></span>

### <span data-ttu-id="063bf-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitConnection</span><span class="sxs-lookup"><span data-stu-id="063bf-123">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitConnection</span></span>

## <span data-ttu-id="063bf-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="063bf-124">NOTES</span></span>

## <span data-ttu-id="063bf-125">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="063bf-125">RELATED LINKS</span></span>

[<span data-ttu-id="063bf-126">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="063bf-126">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="063bf-127">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="063bf-127">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="063bf-128">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="063bf-128">Remove-AzExpressRouteCircuitConnectionConfig</span></span>](Remove-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="063bf-129">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="063bf-129">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="063bf-130">New-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="063bf-130">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)