---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: d98366d9bd3fb42be39f68976e131ec644274431
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179849"
---
# <span data-ttu-id="5328a-101">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="5328a-101">Remove-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="5328a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5328a-102">SYNOPSIS</span></span>
<span data-ttu-id="5328a-103">Entfernt eine vorhandene Express Route-Konfigurations Autorisierung.</span><span class="sxs-lookup"><span data-stu-id="5328a-103">Removes an existing ExpressRoute configuration authorization.</span></span>

## <span data-ttu-id="5328a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5328a-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5328a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5328a-105">DESCRIPTION</span></span>
<span data-ttu-id="5328a-106">Das Cmdlet **Remove-AzExpressRouteCircuitAuthorization** entfernt eine Autorisierung, die einem Express Route-Schaltkreis zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="5328a-106">The **Remove-AzExpressRouteCircuitAuthorization** cmdlet removes an authorization assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="5328a-107">Express Route-Schaltkreise verbinden Ihr lokales Netzwerk mithilfe eines Verbindungs Anbieters anstelle des öffentlichen Internets mit Azure.</span><span class="sxs-lookup"><span data-stu-id="5328a-107">ExpressRoute circuits connect your on-premises network to Azure by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="5328a-108">Der Besitzer eines Express Route-Schaltkreises kann bis zu 10 Berechtigungen für jeden Schaltkreis erstellen. Diese Berechtigungen generieren einen Autorisierungsschlüssel, der von einem virtuellen Netzwerk Besitzer verwendet werden kann, um sein Netzwerk mit dem Schaltkreis zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="5328a-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit.</span></span> <span data-ttu-id="5328a-109">Pro virtuelles Netzwerk kann nur eine Autorisierung vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="5328a-109">There can only be one authorization per virtual network.</span></span> <span data-ttu-id="5328a-110">Der Leitungs Besitzer kann jedoch jederzeit mithilfe von **Remove-AzExpressRouteCircuitAuthorization** die Autorisierung entfernen, die einem virtuellen Netzwerk zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="5328a-110">At any time, however, the circuit owner can use **Remove-AzExpressRouteCircuitAuthorization** to remove the authorization assigned to a virtual network.</span></span> <span data-ttu-id="5328a-111">In diesem Fall ist das entsprechende virtuelle Netzwerk nicht mehr in der Lage, die Express Route-Schaltung zum Herstellen einer Verbindung mit Azure zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="5328a-111">When that happens the corresponding virtual network is no longer able to use the ExpressRoute circuit to connect to Azure.</span></span>

## <span data-ttu-id="5328a-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5328a-112">EXAMPLES</span></span>

### <span data-ttu-id="5328a-113">Beispiel 1: Entfernen einer Schaltkreis Autorisierung von einem Express Route-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="5328a-113">Example 1: Remove a circuit authorization from an ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="5328a-114">In diesem Beispiel wird eine Schaltkreis Autorisierung aus einem Express Route-Schaltkreis entfernt.</span><span class="sxs-lookup"><span data-stu-id="5328a-114">This example removes a circuit authorization from an ExpressRoute circuit.</span></span> <span data-ttu-id="5328a-115">Der erste Befehl verwendet das Cmdlet " **Get-AzExpressRouteCircuit** ", um einen Objektverweis auf einen Express Route-Schaltkreis mit dem Namen ContosoCircuit zu erstellen und das Ergebnis in der Variablen mit dem Namen $Circuit zu speichern.</span><span class="sxs-lookup"><span data-stu-id="5328a-115">The first command uses the **Get-AzExpressRouteCircuit** cmdlet to create an object reference to an ExpressRoute circuit named ContosoCircuit and stores the result in the variable named $Circuit.</span></span>
<span data-ttu-id="5328a-116">Der zweite Befehl kennzeichnet den ContosoCircuitAuthorization für die Schaltkreis Autorisierung zum Entfernen.</span><span class="sxs-lookup"><span data-stu-id="5328a-116">The second command marks the circuit authorization ContosoCircuitAuthorization for removal.</span></span>
<span data-ttu-id="5328a-117">Der dritte Befehl verwendet das Set-AzExpressRouteCircuit-Cmdlet, um die Entfernung des in der $Circuit Variablen gespeicherten Express Route-Schaltkreises zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="5328a-117">The third command uses the Set-AzExpressRouteCircuit cmdlet to confirm the removal of the ExpressRoute circuit stored in the $Circuit variable.</span></span>

## <span data-ttu-id="5328a-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="5328a-118">PARAMETERS</span></span>

### <span data-ttu-id="5328a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5328a-119">-DefaultProfile</span></span>
<span data-ttu-id="5328a-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5328a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5328a-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5328a-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="5328a-122">Gibt das ExpressRouteCircuit-Objekt an, das vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="5328a-122">Specifies the ExpressRouteCircuit object that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5328a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="5328a-123">-Name</span></span>
<span data-ttu-id="5328a-124">Gibt den Namen der Schaltkreis Autorisierung an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="5328a-124">Specifies the name of the circuit authorization that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5328a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5328a-125">CommonParameters</span></span>
<span data-ttu-id="5328a-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5328a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5328a-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5328a-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5328a-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5328a-128">INPUTS</span></span>

### <span data-ttu-id="5328a-129">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5328a-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="5328a-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5328a-130">OUTPUTS</span></span>

### <span data-ttu-id="5328a-131">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5328a-131">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="5328a-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="5328a-132">NOTES</span></span>

## <span data-ttu-id="5328a-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5328a-133">RELATED LINKS</span></span>

[<span data-ttu-id="5328a-134">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="5328a-134">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="5328a-135">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5328a-135">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="5328a-136">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="5328a-136">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="5328a-137">Neu – AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="5328a-137">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="5328a-138">Satz-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5328a-138">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
