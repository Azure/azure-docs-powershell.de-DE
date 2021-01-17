---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 047400472d3f42d5daff0f0ea6aed44455608eb3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472261"
---
# <span data-ttu-id="91b13-101">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="91b13-101">Add-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="91b13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91b13-102">SYNOPSIS</span></span>
<span data-ttu-id="91b13-103">Fügt eine ExpressRoute-Schaltkreisautorisierung hinzu.</span><span class="sxs-lookup"><span data-stu-id="91b13-103">Adds an ExpressRoute circuit authorization.</span></span>

## <span data-ttu-id="91b13-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="91b13-104">SYNTAX</span></span>

```
Add-AzExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91b13-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="91b13-105">DESCRIPTION</span></span>
<span data-ttu-id="91b13-106">Das **Cmdlet "Add-AzExpressRouteCircuitAuthorization"** fügt einem "ExpressRoute"-Schaltkreis eine Autorisierung hinzu.</span><span class="sxs-lookup"><span data-stu-id="91b13-106">The **Add-AzExpressRouteCircuitAuthorization** cmdlet adds an authorization to an ExpressRoute circuit.</span></span> <span data-ttu-id="91b13-107">ExpressRoute-Schaltkreise verbinden Ihr lokales Netzwerk mit der Microsoft-Cloud, indem anstelle des öffentlichen Internets ein Konnektivitätsanbieter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="91b13-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="91b13-108">Der Besitzer eines #A0 kann bis zu 10 Autorisierungen für jeden Schaltkreis erstellen. diese Autorisierungen generieren einen Autorisierungsschlüssel, der von einem virtuellen Netzwerkbesitzer verwendet werden kann, um sein Netzwerk mit dem Schaltkreis zu verbinden (eine Autorisierung pro virtuellem Netzwerk).</span><span class="sxs-lookup"><span data-stu-id="91b13-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="91b13-109">**Add-AzExpressRouteCircuitAuthorization** fügt einem Schaltkreis eine neue Autorisierung hinzu und generiert gleichzeitig den entsprechenden Autorisierungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="91b13-109">**Add-AzExpressRouteCircuitAuthorization** adds a new authorization to a circuit and, at the same time, generates the corresponding authorization key.</span></span> <span data-ttu-id="91b13-110">Diese Schlüssel können jederzeit angezeigt werden, indem Sie das Cmdlet Get-AzExpressRouteCircuitAuthorization ausführen, und können dann nach Bedarf kopiert und an den entsprechenden Netzwerkbesitzer weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="91b13-110">These keys can be viewed at any time by running the Get-AzExpressRouteCircuitAuthorization cmdlet and, as needed, can then be copied and forwarded to the appropriate network owner.</span></span>
<span data-ttu-id="91b13-111">Beachten Sie, dass Sie nach der Ausführung von **"Add-AzExpressRouteCircuitAuthorization"** das cmdlet Set-AzExpressRouteCircuit aufrufen müssen, um den Schlüssel zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="91b13-111">Note that, after running **Add-AzExpressRouteCircuitAuthorization**, you must call the Set-AzExpressRouteCircuit cmdlet to activate the key.</span></span> <span data-ttu-id="91b13-112">Wenn Sie **Set-AzExpressRouteCircuit** nicht aufrufen, wird die Autorisierung dem Schaltkreis hinzugefügt, aber nicht für die Verwendung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="91b13-112">If you do not call **Set-AzExpressRouteCircuit** the authorization will be added to the circuit but will not be enabled for use.</span></span>

## <span data-ttu-id="91b13-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="91b13-113">EXAMPLES</span></span>

### <span data-ttu-id="91b13-114">Beispiel 1: Hinzufügen einer Autorisierung zum angegebenen "ExpressRoute"-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="91b13-114">Example 1: Add an authorization to the specified ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="91b13-115">Mit den Befehlen in diesem Beispiel wird eine neue Autorisierung zu einem vorhandenen "ExpressRoute"-Schaltkreis hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="91b13-115">The commands in this example add a new authorization to an existing ExpressRoute circuit.</span></span> <span data-ttu-id="91b13-116">Der erste Befehl verwendet **"Get-AzExpressRouteCircuit",** um einen Objektverweis auf einen Schaltkreis namens "ContosoCircuit" zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="91b13-116">The first command uses **Get-AzExpressRouteCircuit** to create an object reference to a circuit named ContosoCircuit.</span></span> <span data-ttu-id="91b13-117">Dieser Objektverweis wird in einer Variablen mit dem Namen $Circuit.</span><span class="sxs-lookup"><span data-stu-id="91b13-117">That object reference is stored in a variable named $Circuit.</span></span>
<span data-ttu-id="91b13-118">Im zweiten Befehl wird das **Cmdlet "Add-AzExpressRouteCircuitAuthorization"** verwendet, um dem "ExpressRoute"-Schaltkreis eine neue Autorisierung (ContosoCircuitAuthorization) hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="91b13-118">In the second command, the **Add-AzExpressRouteCircuitAuthorization** cmdlet is used to add a new authorization (ContosoCircuitAuthorization) to the ExpressRoute circuit.</span></span> <span data-ttu-id="91b13-119">Dieser Befehl fügt die Autorisierung hinzu, aktiviert diese Autorisierung jedoch nicht.</span><span class="sxs-lookup"><span data-stu-id="91b13-119">This command adds the authorization but does not activate that authorization.</span></span> <span data-ttu-id="91b13-120">Zum Aktivieren einer Autorisierung ist das im endgültigen Befehl im Beispiel gezeigte **Set-AzExpressRouteCircuit** erforderlich.</span><span class="sxs-lookup"><span data-stu-id="91b13-120">Activating an authorization requires the **Set-AzExpressRouteCircuit** shown in the final command in the example.</span></span>

## <span data-ttu-id="91b13-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91b13-121">PARAMETERS</span></span>

### <span data-ttu-id="91b13-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91b13-122">-DefaultProfile</span></span>
<span data-ttu-id="91b13-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="91b13-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91b13-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="91b13-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="91b13-125">Gibt den ExpressRoute-Schaltkreis an, dem dieses Cmdlet die Autorisierung hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="91b13-125">Specifies the ExpressRoute circuit that this cmdlet adds the authorization to.</span></span>

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

### <span data-ttu-id="91b13-126">-Name</span><span class="sxs-lookup"><span data-stu-id="91b13-126">-Name</span></span>
<span data-ttu-id="91b13-127">Gibt den Namen der Schaltkreisautorisierung an, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="91b13-127">Specifies the name of the circuit authorization to be added.</span></span>

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

### <span data-ttu-id="91b13-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91b13-128">CommonParameters</span></span>
<span data-ttu-id="91b13-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91b13-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91b13-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91b13-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91b13-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="91b13-131">INPUTS</span></span>

### <span data-ttu-id="91b13-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="91b13-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="91b13-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="91b13-133">OUTPUTS</span></span>

### <span data-ttu-id="91b13-134">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="91b13-134">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="91b13-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="91b13-135">NOTES</span></span>

## <span data-ttu-id="91b13-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="91b13-136">RELATED LINKS</span></span>

[<span data-ttu-id="91b13-137">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="91b13-137">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="91b13-138">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="91b13-138">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="91b13-139">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="91b13-139">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="91b13-140">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="91b13-140">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="91b13-141">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="91b13-141">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
