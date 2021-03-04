---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 2adb971d2e44f844fe52bb83a9ce834bbebe1897
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941683"
---
# <span data-ttu-id="b6728-101">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="b6728-101">Remove-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="b6728-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6728-102">SYNOPSIS</span></span>
<span data-ttu-id="b6728-103">Entfernt eine vorhandene ExpressRoute-Konfigurationsautorisierung.</span><span class="sxs-lookup"><span data-stu-id="b6728-103">Removes an existing ExpressRoute configuration authorization.</span></span>

## <span data-ttu-id="b6728-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b6728-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6728-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b6728-105">DESCRIPTION</span></span>
<span data-ttu-id="b6728-106">Das **Cmdlet Remove-AzExpressRouteCircuitAuthorization** entfernt eine Autorisierung, die einem ExpressRoute-Schaltkreis zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="b6728-106">The **Remove-AzExpressRouteCircuitAuthorization** cmdlet removes an authorization assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="b6728-107">ExpressRoute-Schaltkreise verbinden Ihr lokales Netzwerk mit Azure mithilfe eines Konnektivitätsanbieters anstelle des öffentlichen Internets.</span><span class="sxs-lookup"><span data-stu-id="b6728-107">ExpressRoute circuits connect your on-premises network to Azure by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="b6728-108">Der Besitzer eines #A0 kann bis zu 10 Berechtigungen für jeden Schaltkreis erstellen. Diese Autorisierungen generieren einen Autorisierungsschlüssel, der von einem Besitzer eines virtuellen Netzwerks verwendet werden kann, um sein Netzwerk mit dem Schaltkreis zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="b6728-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit.</span></span> <span data-ttu-id="b6728-109">Es kann nur eine Autorisierung pro virtuellem Netzwerk gibt.</span><span class="sxs-lookup"><span data-stu-id="b6728-109">There can only be one authorization per virtual network.</span></span> <span data-ttu-id="b6728-110">Der Besitzer des Schaltkreises kann jedoch **jederzeit Remove-AzExpressRouteCircuitAuthorization** verwenden, um die einem virtuellen Netzwerk zugewiesene Autorisierung zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="b6728-110">At any time, however, the circuit owner can use **Remove-AzExpressRouteCircuitAuthorization** to remove the authorization assigned to a virtual network.</span></span> <span data-ttu-id="b6728-111">In diesem Fall kann das entsprechende virtuelle Netzwerk den ExpressRoute-Schaltkreis nicht mehr verwenden, um eine Verbindung mit Azure herzustellen.</span><span class="sxs-lookup"><span data-stu-id="b6728-111">When that happens the corresponding virtual network is no longer able to use the ExpressRoute circuit to connect to Azure.</span></span>

## <span data-ttu-id="b6728-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b6728-112">EXAMPLES</span></span>

### <span data-ttu-id="b6728-113">Beispiel 1: Entfernen einer Schaltungsautorisierung von einem ExpressRoute-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="b6728-113">Example 1: Remove a circuit authorization from an ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="b6728-114">In diesem Beispiel wird eine Schaltungsautorisierung aus einem ExpressRoute-Schaltkreis entfernt.</span><span class="sxs-lookup"><span data-stu-id="b6728-114">This example removes a circuit authorization from an ExpressRoute circuit.</span></span> <span data-ttu-id="b6728-115">Der erste Befehl verwendet das **Get-AzExpressRouteCircuit-Cmdlet,** um einen Objektverweis auf einen ExpressRoute-Schaltkreis namens ContosoCircuit zu erstellen, und speichert das Ergebnis in der Variablen namens $Circuit.</span><span class="sxs-lookup"><span data-stu-id="b6728-115">The first command uses the **Get-AzExpressRouteCircuit** cmdlet to create an object reference to an ExpressRoute circuit named ContosoCircuit and stores the result in the variable named $Circuit.</span></span>
<span data-ttu-id="b6728-116">Der zweite Befehl kennzeichnet die Schaltkreisautorisierung ContosoCircuitAuthorization zum Entfernen.</span><span class="sxs-lookup"><span data-stu-id="b6728-116">The second command marks the circuit authorization ContosoCircuitAuthorization for removal.</span></span>
<span data-ttu-id="b6728-117">Der dritte Befehl verwendet das Set-AzExpressRouteCircuit-Cmdlet, um das Entfernen des in der Variablen $Circuit ExpressRoute-Schaltkreises zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="b6728-117">The third command uses the Set-AzExpressRouteCircuit cmdlet to confirm the removal of the ExpressRoute circuit stored in the $Circuit variable.</span></span>

## <span data-ttu-id="b6728-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b6728-118">PARAMETERS</span></span>

### <span data-ttu-id="b6728-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6728-119">-DefaultProfile</span></span>
<span data-ttu-id="b6728-120">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b6728-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6728-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b6728-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="b6728-122">Gibt das ExpressRouteCircuit-Objekt an, das von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="b6728-122">Specifies the ExpressRouteCircuit object that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b6728-123">-Name</span><span class="sxs-lookup"><span data-stu-id="b6728-123">-Name</span></span>
<span data-ttu-id="b6728-124">Gibt den Namen der Schaltkreisautorisierung an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="b6728-124">Specifies the name of the circuit authorization that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b6728-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6728-125">CommonParameters</span></span>
<span data-ttu-id="b6728-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6728-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6728-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6728-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6728-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b6728-128">INPUTS</span></span>

### <span data-ttu-id="b6728-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b6728-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="b6728-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b6728-130">OUTPUTS</span></span>

### <span data-ttu-id="b6728-131">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b6728-131">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="b6728-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b6728-132">NOTES</span></span>

## <span data-ttu-id="b6728-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b6728-133">RELATED LINKS</span></span>

[<span data-ttu-id="b6728-134">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="b6728-134">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="b6728-135">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b6728-135">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="b6728-136">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="b6728-136">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="b6728-137">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="b6728-137">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="b6728-138">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="b6728-138">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
