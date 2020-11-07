---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 38D57CE4-6994-4BDA-A50E-28680EF4E568
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: af8490ab242919d44b0b1b47c9cab92674e9df9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665356"
---
# <span data-ttu-id="6f515-101">Remove-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="6f515-101">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="6f515-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6f515-102">SYNOPSIS</span></span>
<span data-ttu-id="6f515-103">Entfernt eine vorhandene Express Route-Konfigurations Autorisierung.</span><span class="sxs-lookup"><span data-stu-id="6f515-103">Removes an existing ExpressRoute configuration authorization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f515-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f515-104">SYNTAX</span></span>

```
Remove-AzureRmExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f515-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6f515-105">DESCRIPTION</span></span>
<span data-ttu-id="6f515-106">Das Cmdlet **Remove-AzureRmExpressRouteCircuitAuthorization** entfernt eine Autorisierung, die einem Express Route-Schaltkreis zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="6f515-106">The **Remove-AzureRmExpressRouteCircuitAuthorization** cmdlet removes an authorization assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="6f515-107">Express Route-Schaltkreise verbinden Ihr lokales Netzwerk mithilfe eines Verbindungs Anbieters anstelle des öffentlichen Internets mit Azure.</span><span class="sxs-lookup"><span data-stu-id="6f515-107">ExpressRoute circuits connect your on-premises network to Azure by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="6f515-108">Der Besitzer eines Express Route-Schaltkreises kann bis zu 10 Berechtigungen für jeden Schaltkreis erstellen. Diese Berechtigungen generieren einen Autorisierungsschlüssel, der von einem virtuellen Netzwerk Besitzer verwendet werden kann, um sein Netzwerk mit dem Schaltkreis zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="6f515-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit.</span></span> <span data-ttu-id="6f515-109">Pro virtuelles Netzwerk kann nur eine Autorisierung vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="6f515-109">There can only be one authorization per virtual network.</span></span> <span data-ttu-id="6f515-110">Der Leitungs Besitzer kann jedoch jederzeit mithilfe von **Remove-AzureRmExpressRouteCircuitAuthorization** die Autorisierung entfernen, die einem virtuellen Netzwerk zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="6f515-110">At any time, however, the circuit owner can use **Remove-AzureRmExpressRouteCircuitAuthorization** to remove the authorization assigned to a virtual network.</span></span> <span data-ttu-id="6f515-111">In diesem Fall ist das entsprechende virtuelle Netzwerk nicht mehr in der Lage, die Express Route-Schaltung zum Herstellen einer Verbindung mit Azure zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="6f515-111">When that happens the corresponding virtual network is no longer able to use the ExpressRoute circuit to connect to Azure.</span></span>

## <span data-ttu-id="6f515-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6f515-112">EXAMPLES</span></span>

### <span data-ttu-id="6f515-113">Beispiel 1: Entfernen einer Schaltkreis Autorisierung von einem Express Route-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="6f515-113">Example 1: Remove a circuit authorization from an ExpressRoute circuit</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Remove-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="6f515-114">In diesem Beispiel wird eine Schaltkreis Autorisierung aus einem Express Route-Schaltkreis entfernt.</span><span class="sxs-lookup"><span data-stu-id="6f515-114">This example removes a circuit authorization from an ExpressRoute circuit.</span></span> <span data-ttu-id="6f515-115">Der erste Befehl verwendet das Cmdlet " **Get-AzureRmExpressRouteCircuit** ", um einen Objektverweis auf einen Express Route-Schaltkreis mit dem Namen ContosoCircuit zu erstellen und das Ergebnis in der Variablen mit dem Namen $Circuit zu speichern.</span><span class="sxs-lookup"><span data-stu-id="6f515-115">The first command uses the **Get-AzureRmExpressRouteCircuit** cmdlet to create an object reference to an ExpressRoute circuit named ContosoCircuit and stores the result in the variable named $Circuit.</span></span>

<span data-ttu-id="6f515-116">Der zweite Befehl kennzeichnet den ContosoCircuitAuthorization für die Schaltkreis Autorisierung zum Entfernen.</span><span class="sxs-lookup"><span data-stu-id="6f515-116">The second command marks the circuit authorization ContosoCircuitAuthorization for removal.</span></span>

<span data-ttu-id="6f515-117">Der dritte Befehl verwendet das Set-AzureRmExpressRouteCircuit-Cmdlet, um die Entfernung des in der $Circuit Variablen gespeicherten Express Route-Schaltkreises zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="6f515-117">The third command uses the Set-AzureRmExpressRouteCircuit cmdlet to confirm the removal of the ExpressRoute circuit stored in the $Circuit variable.</span></span>

## <span data-ttu-id="6f515-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f515-118">PARAMETERS</span></span>

### <span data-ttu-id="6f515-119">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6f515-119">-ExpressRouteCircuit</span></span>
<span data-ttu-id="6f515-120">Gibt das ExpressRouteCircuit-Objekt an, das vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="6f515-120">Specifies the ExpressRouteCircuit object that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6f515-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6f515-121">-Name</span></span>
<span data-ttu-id="6f515-122">Gibt den Namen der Schaltkreis Autorisierung an, die vom Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="6f515-122">Specifies the name of the circuit authorization that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6f515-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f515-123">-DefaultProfile</span></span>
<span data-ttu-id="6f515-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6f515-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f515-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f515-125">CommonParameters</span></span>
<span data-ttu-id="6f515-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f515-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f515-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f515-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f515-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6f515-128">INPUTS</span></span>

### <span data-ttu-id="6f515-129">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6f515-129">PSExpressRouteCircuit</span></span>
<span data-ttu-id="6f515-130">Dieses Cmdlet akzeptiert Pipelineinstanzen des **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="6f515-130">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="6f515-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6f515-131">OUTPUTS</span></span>

### <span data-ttu-id="6f515-132">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6f515-132">PSExpressRouteCircuit</span></span>
<span data-ttu-id="6f515-133">Dieses Cmdlet ändert vorhandene Instanzen des **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="6f515-133">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="6f515-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="6f515-134">NOTES</span></span>

## <span data-ttu-id="6f515-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6f515-135">RELATED LINKS</span></span>

[<span data-ttu-id="6f515-136">Add-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="6f515-136">Add-AzureRmExpressRouteCircuitAuthorization</span></span>](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="6f515-137">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6f515-137">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="6f515-138">Get-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="6f515-138">Get-AzureRmExpressRouteCircuitAuthorization</span></span>](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="6f515-139">Neu – AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="6f515-139">New-AzureRmExpressRouteCircuitAuthorization</span></span>](./New-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="6f515-140">Satz-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="6f515-140">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
