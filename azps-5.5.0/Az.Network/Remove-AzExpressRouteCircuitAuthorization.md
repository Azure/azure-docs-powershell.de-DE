---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: d98366d9bd3fb42be39f68976e131ec644274431
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159009"
---
# <span data-ttu-id="8822f-101">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="8822f-101">Remove-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="8822f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8822f-102">SYNOPSIS</span></span>
<span data-ttu-id="8822f-103">Entfernt eine vorhandene ExpressRoute-Konfigurationsautorisierung.</span><span class="sxs-lookup"><span data-stu-id="8822f-103">Removes an existing ExpressRoute configuration authorization.</span></span>

## <span data-ttu-id="8822f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8822f-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8822f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8822f-105">DESCRIPTION</span></span>
<span data-ttu-id="8822f-106">Mit **dem Cmdlet "Remove-AzExpressRouteCircuitAuthorization"** wird eine einem "ExpressRoute"-Schaltkreis zugewiesene Autorisierung entfernt.</span><span class="sxs-lookup"><span data-stu-id="8822f-106">The **Remove-AzExpressRouteCircuitAuthorization** cmdlet removes an authorization assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="8822f-107">ExpressRoute-Schaltkreise verbinden Ihr lokales Netzwerk mit Azure, indem ein Konnektivitätsanbieter anstelle des öffentlichen Internets verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8822f-107">ExpressRoute circuits connect your on-premises network to Azure by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="8822f-108">Der Besitzer eines #A0 kann bis zu 10 Autorisierungen für jeden Schaltkreis erstellen. diese Autorisierungen generieren einen Autorisierungsschlüssel, der von einem virtuellen Netzwerkbesitzer verwendet werden kann, um sein Netzwerk mit dem Schaltkreis zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="8822f-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit.</span></span> <span data-ttu-id="8822f-109">Pro virtuellem Netzwerk kann es nur eine Autorisierung gibt.</span><span class="sxs-lookup"><span data-stu-id="8822f-109">There can only be one authorization per virtual network.</span></span> <span data-ttu-id="8822f-110">Der Besitzer des Schaltkreises kann jedoch **jederzeit "Remove-AzExpressRouteCircuitAuthorization"** verwenden, um die einem virtuellen Netzwerk zugewiesene Autorisierung zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="8822f-110">At any time, however, the circuit owner can use **Remove-AzExpressRouteCircuitAuthorization** to remove the authorization assigned to a virtual network.</span></span> <span data-ttu-id="8822f-111">In diesem Fall kann das entsprechende virtuelle Netzwerk den "ExpressRoute"-Schaltkreis nicht mehr zum Herstellen einer Verbindung mit Azure verwenden.</span><span class="sxs-lookup"><span data-stu-id="8822f-111">When that happens the corresponding virtual network is no longer able to use the ExpressRoute circuit to connect to Azure.</span></span>

## <span data-ttu-id="8822f-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8822f-112">EXAMPLES</span></span>

### <span data-ttu-id="8822f-113">Beispiel 1: Entfernen einer Schaltkreisautorisierung von einem ExpressRoute-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="8822f-113">Example 1: Remove a circuit authorization from an ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="8822f-114">In diesem Beispiel wird eine Schaltkreisautorisierung von einem "ExpressRoute"-Schaltkreis entfernt.</span><span class="sxs-lookup"><span data-stu-id="8822f-114">This example removes a circuit authorization from an ExpressRoute circuit.</span></span> <span data-ttu-id="8822f-115">Der erste Befehl verwendet das **Cmdlet "Get-AzExpressRouteCircuit",** um einen Objektverweis auf einen "ContosoCircuit"-Schaltkreis zu erstellen, und speichert das Ergebnis in der Variablen namens $Circuit.</span><span class="sxs-lookup"><span data-stu-id="8822f-115">The first command uses the **Get-AzExpressRouteCircuit** cmdlet to create an object reference to an ExpressRoute circuit named ContosoCircuit and stores the result in the variable named $Circuit.</span></span>
<span data-ttu-id="8822f-116">Der zweite Befehl kennzeichnet die Schaltkreisautorisierung "ContosoCircuitAuthorization" zum Entfernen.</span><span class="sxs-lookup"><span data-stu-id="8822f-116">The second command marks the circuit authorization ContosoCircuitAuthorization for removal.</span></span>
<span data-ttu-id="8822f-117">Der dritte Befehl verwendet das Set-AzExpressRouteCircuit Cmdlet, um das Entfernen des in der Variablen gespeicherten $Circuit zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="8822f-117">The third command uses the Set-AzExpressRouteCircuit cmdlet to confirm the removal of the ExpressRoute circuit stored in the $Circuit variable.</span></span>

## <span data-ttu-id="8822f-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8822f-118">PARAMETERS</span></span>

### <span data-ttu-id="8822f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8822f-119">-DefaultProfile</span></span>
<span data-ttu-id="8822f-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8822f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8822f-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8822f-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="8822f-122">Gibt das ExpressRouteCircuit-Objekt an, das von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="8822f-122">Specifies the ExpressRouteCircuit object that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8822f-123">-Name</span><span class="sxs-lookup"><span data-stu-id="8822f-123">-Name</span></span>
<span data-ttu-id="8822f-124">Gibt den Namen der Schaltkreisautorisierung an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="8822f-124">Specifies the name of the circuit authorization that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8822f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8822f-125">CommonParameters</span></span>
<span data-ttu-id="8822f-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8822f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8822f-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8822f-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8822f-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8822f-128">INPUTS</span></span>

### <span data-ttu-id="8822f-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8822f-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="8822f-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8822f-130">OUTPUTS</span></span>

### <span data-ttu-id="8822f-131">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8822f-131">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="8822f-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8822f-132">NOTES</span></span>

## <span data-ttu-id="8822f-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8822f-133">RELATED LINKS</span></span>

[<span data-ttu-id="8822f-134">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="8822f-134">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="8822f-135">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8822f-135">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="8822f-136">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="8822f-136">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="8822f-137">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="8822f-137">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="8822f-138">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="8822f-138">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
