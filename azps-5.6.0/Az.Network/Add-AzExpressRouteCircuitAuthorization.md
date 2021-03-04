---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/powershell/module/az.network/add-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 9812316b20db927dea9bfe999cad54fe002bfc93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918768"
---
# <span data-ttu-id="a3ad4-101">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="a3ad4-101">Add-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="a3ad4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3ad4-102">SYNOPSIS</span></span>
<span data-ttu-id="a3ad4-103">Fügt eine ExpressRoute-Schaltungsautorisierung hinzu.</span><span class="sxs-lookup"><span data-stu-id="a3ad4-103">Adds an ExpressRoute circuit authorization.</span></span>

## <span data-ttu-id="a3ad4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a3ad4-104">SYNTAX</span></span>

```
Add-AzExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3ad4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a3ad4-105">DESCRIPTION</span></span>
<span data-ttu-id="a3ad4-106">Das **Add-AzExpressRouteCircuitAuthorization-Cmdlet** fügt einer ExpressRoute-Schaltung eine Autorisierung hinzu.</span><span class="sxs-lookup"><span data-stu-id="a3ad4-106">The **Add-AzExpressRouteCircuitAuthorization** cmdlet adds an authorization to an ExpressRoute circuit.</span></span> <span data-ttu-id="a3ad4-107">ExpressRoute-Schaltkreise verbinden Ihr lokales Netzwerk mit der Microsoft-Cloud, indem sie einen Konnektivitätsanbieter anstelle des öffentlichen Internets verwenden.</span><span class="sxs-lookup"><span data-stu-id="a3ad4-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="a3ad4-108">Der Besitzer eines #A0 kann bis zu 10 Berechtigungen für jeden Schaltkreis erstellen. Diese Autorisierungen generieren einen Autorisierungsschlüssel, der von einem Besitzer des virtuellen Netzwerks verwendet werden kann, um sein Netzwerk mit dem Schaltkreis zu verbinden (eine Autorisierung pro virtuellem Netzwerk).</span><span class="sxs-lookup"><span data-stu-id="a3ad4-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="a3ad4-109">**Add-AzExpressRouteCircuitAuthorization** fügt einem Schaltkreis eine neue Autorisierung hinzu und generiert gleichzeitig den entsprechenden Autorisierungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="a3ad4-109">**Add-AzExpressRouteCircuitAuthorization** adds a new authorization to a circuit and, at the same time, generates the corresponding authorization key.</span></span> <span data-ttu-id="a3ad4-110">Diese Schlüssel können jederzeit angezeigt werden, indem sie das Get-AzExpressRouteCircuitAuthorization-Cmdlet ausführen und dann nach Bedarf kopiert und an den entsprechenden Netzwerkbesitzer weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="a3ad4-110">These keys can be viewed at any time by running the Get-AzExpressRouteCircuitAuthorization cmdlet and, as needed, can then be copied and forwarded to the appropriate network owner.</span></span>
<span data-ttu-id="a3ad4-111">Beachten Sie, dass Sie nach dem Ausführen von **Add-AzExpressRouteCircuitAuthorization** das cmdlet Set-AzExpressRouteCircuit aufrufen müssen, um den Schlüssel zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a3ad4-111">Note that, after running **Add-AzExpressRouteCircuitAuthorization**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the key.</span></span> <span data-ttu-id="a3ad4-112">Wenn Sie **Set-AzExpressRouteCircuit** nicht aufrufen, wird die Autorisierung dem Schaltkreis hinzugefügt, aber nicht für die Verwendung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a3ad4-112">If you do not call **Set-AzExpressRouteCircuit** the authorization will be added to the circuit but will not be enabled for use.</span></span>

## <span data-ttu-id="a3ad4-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a3ad4-113">EXAMPLES</span></span>

### <span data-ttu-id="a3ad4-114">Beispiel 1: Hinzufügen einer Autorisierung zum angegebenen ExpressRoute-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="a3ad4-114">Example 1: Add an authorization to the specified ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="a3ad4-115">Die Befehle in diesem Beispiel fügen einer vorhandenen ExpressRoute-Schaltung eine neue Autorisierung hinzu.</span><span class="sxs-lookup"><span data-stu-id="a3ad4-115">The commands in this example add a new authorization to an existing ExpressRoute circuit.</span></span> <span data-ttu-id="a3ad4-116">Der erste Befehl verwendet **Get-AzExpressRouteCircuit,** um einen Objektverweis auf einen Schaltkreis namens ContosoCircuit zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a3ad4-116">The first command uses **Get-AzExpressRouteCircuit** to create an object reference to a circuit named ContosoCircuit.</span></span> <span data-ttu-id="a3ad4-117">Dieser Objektverweis wird in einer Variablen mit dem Namen $Circuit.</span><span class="sxs-lookup"><span data-stu-id="a3ad4-117">That object reference is stored in a variable named $Circuit.</span></span>
<span data-ttu-id="a3ad4-118">Im zweiten Befehl wird das **Add-AzExpressRouteCircuitAuthorization-Cmdlet** verwendet, um dem ExpressRoute-Schaltkreis eine neue Autorisierung (ContosoCircuitAuthorization) hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="a3ad4-118">In the second command, the **Add-AzExpressRouteCircuitAuthorization** cmdlet is used to add a new authorization (ContosoCircuitAuthorization) to the ExpressRoute circuit.</span></span> <span data-ttu-id="a3ad4-119">Dieser Befehl fügt die Autorisierung hinzu, aktiviert diese Autorisierung aber nicht.</span><span class="sxs-lookup"><span data-stu-id="a3ad4-119">This command adds the authorization but does not activate that authorization.</span></span> <span data-ttu-id="a3ad4-120">Zum Aktivieren einer Autorisierung ist **das Set-AzExpressRouteCircuit** erforderlich, das im letzten Befehl im Beispiel angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a3ad4-120">Activating an authorization requires the **Set-AzExpressRouteCircuit** shown in the final command in the example.</span></span>

## <span data-ttu-id="a3ad4-121">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a3ad4-121">PARAMETERS</span></span>

### <span data-ttu-id="a3ad4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3ad4-122">-DefaultProfile</span></span>
<span data-ttu-id="a3ad4-123">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a3ad4-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3ad4-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a3ad4-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="a3ad4-125">Gibt den ExpressRoute-Schaltkreis an, dem dieses Cmdlet die Autorisierung hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="a3ad4-125">Specifies the ExpressRoute circuit that this cmdlet adds the authorization to.</span></span>

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

### <span data-ttu-id="a3ad4-126">-Name</span><span class="sxs-lookup"><span data-stu-id="a3ad4-126">-Name</span></span>
<span data-ttu-id="a3ad4-127">Gibt den Namen der zu hinzufügenden Schaltkreisautorisierung an.</span><span class="sxs-lookup"><span data-stu-id="a3ad4-127">Specifies the name of the circuit authorization to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3ad4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3ad4-128">CommonParameters</span></span>
<span data-ttu-id="a3ad4-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3ad4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3ad4-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3ad4-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3ad4-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a3ad4-131">INPUTS</span></span>

### <span data-ttu-id="a3ad4-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a3ad4-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="a3ad4-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a3ad4-133">OUTPUTS</span></span>

### <span data-ttu-id="a3ad4-134">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a3ad4-134">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="a3ad4-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a3ad4-135">NOTES</span></span>

## <span data-ttu-id="a3ad4-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a3ad4-136">RELATED LINKS</span></span>

[<span data-ttu-id="a3ad4-137">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a3ad4-137">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="a3ad4-138">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="a3ad4-138">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="a3ad4-139">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="a3ad4-139">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="a3ad4-140">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="a3ad4-140">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="a3ad4-141">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="a3ad4-141">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
