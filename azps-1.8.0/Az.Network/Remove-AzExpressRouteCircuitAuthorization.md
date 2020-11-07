---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 62cfc4fc3555b9eb798a1d64c53b0b25e9abc14c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660388"
---
# <span data-ttu-id="ec78f-101">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="ec78f-101">Remove-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="ec78f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ec78f-102">SYNOPSIS</span></span>
<span data-ttu-id="ec78f-103">Entfernt eine vorhandene Express Route-Konfigurations Autorisierung.</span><span class="sxs-lookup"><span data-stu-id="ec78f-103">Removes an existing ExpressRoute configuration authorization.</span></span>

## <span data-ttu-id="ec78f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec78f-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec78f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ec78f-105">DESCRIPTION</span></span>
<span data-ttu-id="ec78f-106">Das Cmdlet **Remove-AzExpressRouteCircuitAuthorization** entfernt eine Autorisierung, die einem Express Route-Schaltkreis zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="ec78f-106">The **Remove-AzExpressRouteCircuitAuthorization** cmdlet removes an authorization assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="ec78f-107">Express Route-Schaltkreise verbinden Ihr lokales Netzwerk mithilfe eines Verbindungs Anbieters anstelle des öffentlichen Internets mit Azure.</span><span class="sxs-lookup"><span data-stu-id="ec78f-107">ExpressRoute circuits connect your on-premises network to Azure by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="ec78f-108">Der Besitzer eines Express Route-Schaltkreises kann bis zu 10 Berechtigungen für jeden Schaltkreis erstellen. Diese Berechtigungen generieren einen Autorisierungsschlüssel, der von einem virtuellen Netzwerk Besitzer verwendet werden kann, um sein Netzwerk mit dem Schaltkreis zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="ec78f-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit.</span></span> <span data-ttu-id="ec78f-109">Pro virtuelles Netzwerk kann nur eine Autorisierung vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="ec78f-109">There can only be one authorization per virtual network.</span></span> <span data-ttu-id="ec78f-110">Der Leitungs Besitzer kann jedoch jederzeit mithilfe von **Remove-AzExpressRouteCircuitAuthorization** die Autorisierung entfernen, die einem virtuellen Netzwerk zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="ec78f-110">At any time, however, the circuit owner can use **Remove-AzExpressRouteCircuitAuthorization** to remove the authorization assigned to a virtual network.</span></span> <span data-ttu-id="ec78f-111">In diesem Fall ist das entsprechende virtuelle Netzwerk nicht mehr in der Lage, die Express Route-Schaltung zum Herstellen einer Verbindung mit Azure zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ec78f-111">When that happens the corresponding virtual network is no longer able to use the ExpressRoute circuit to connect to Azure.</span></span>

## <span data-ttu-id="ec78f-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ec78f-112">EXAMPLES</span></span>

### <span data-ttu-id="ec78f-113">Beispiel 1: Entfernen einer Schaltkreis Autorisierung von einem Express Route-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="ec78f-113">Example 1: Remove a circuit authorization from an ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="ec78f-114">In diesem Beispiel wird eine Schaltkreis Autorisierung aus einem Express Route-Schaltkreis entfernt.</span><span class="sxs-lookup"><span data-stu-id="ec78f-114">This example removes a circuit authorization from an ExpressRoute circuit.</span></span> <span data-ttu-id="ec78f-115">Der erste Befehl verwendet das Cmdlet " **Get-AzExpressRouteCircuit** ", um einen Objektverweis auf einen Express Route-Schaltkreis mit dem Namen ContosoCircuit zu erstellen und das Ergebnis in der Variablen mit dem Namen $Circuit zu speichern.</span><span class="sxs-lookup"><span data-stu-id="ec78f-115">The first command uses the **Get-AzExpressRouteCircuit** cmdlet to create an object reference to an ExpressRoute circuit named ContosoCircuit and stores the result in the variable named $Circuit.</span></span>
<span data-ttu-id="ec78f-116">Der zweite Befehl kennzeichnet den ContosoCircuitAuthorization für die Schaltkreis Autorisierung zum Entfernen.</span><span class="sxs-lookup"><span data-stu-id="ec78f-116">The second command marks the circuit authorization ContosoCircuitAuthorization for removal.</span></span>
<span data-ttu-id="ec78f-117">Der dritte Befehl verwendet das Set-AzExpressRouteCircuit-Cmdlet, um die Entfernung des in der $Circuit Variablen gespeicherten Express Route-Schaltkreises zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="ec78f-117">The third command uses the Set-AzExpressRouteCircuit cmdlet to confirm the removal of the ExpressRoute circuit stored in the $Circuit variable.</span></span>

## <span data-ttu-id="ec78f-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec78f-118">PARAMETERS</span></span>

### <span data-ttu-id="ec78f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec78f-119">-DefaultProfile</span></span>
<span data-ttu-id="ec78f-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ec78f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec78f-121">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ec78f-121">-ExpressRouteCircuit</span></span>
<span data-ttu-id="ec78f-122">Gibt das ExpressRouteCircuit-Objekt an, das vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="ec78f-122">Specifies the ExpressRouteCircuit object that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ec78f-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ec78f-123">-Name</span></span>
<span data-ttu-id="ec78f-124">Gibt den Namen der Schaltkreis Autorisierung an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="ec78f-124">Specifies the name of the circuit authorization that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ec78f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec78f-125">CommonParameters</span></span>
<span data-ttu-id="ec78f-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec78f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec78f-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec78f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec78f-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ec78f-128">INPUTS</span></span>

### <span data-ttu-id="ec78f-129">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ec78f-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="ec78f-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ec78f-130">OUTPUTS</span></span>

### <span data-ttu-id="ec78f-131">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ec78f-131">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="ec78f-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="ec78f-132">NOTES</span></span>

## <span data-ttu-id="ec78f-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ec78f-133">RELATED LINKS</span></span>

[<span data-ttu-id="ec78f-134">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="ec78f-134">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="ec78f-135">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ec78f-135">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="ec78f-136">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="ec78f-136">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="ec78f-137">Neu – AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="ec78f-137">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="ec78f-138">Satz-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ec78f-138">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
