---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermexpressroutecircuitauthorization
schema: 2.0.0
ms.openlocfilehash: 9b41eb0c95c2b1693e56c8b11fee86b6e49a4609
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849259"
---
# <span data-ttu-id="af80c-101">Add-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="af80c-101">Add-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="af80c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="af80c-102">SYNOPSIS</span></span>
<span data-ttu-id="af80c-103">Fügt eine Express Route-Schaltkreis Autorisierung hinzu.</span><span class="sxs-lookup"><span data-stu-id="af80c-103">Adds an ExpressRoute circuit authorization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af80c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="af80c-104">SYNTAX</span></span>

```
Add-AzureRmExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af80c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="af80c-105">DESCRIPTION</span></span>
<span data-ttu-id="af80c-106">Mit dem Cmdlet **Add-AzureRmExpressRouteCircuitAuthorization** wird eine Autorisierung zu einem Express Route-Schaltkreis hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="af80c-106">The **Add-AzureRmExpressRouteCircuitAuthorization** cmdlet adds an authorization to an ExpressRoute circuit.</span></span> <span data-ttu-id="af80c-107">Express Route-Schaltkreise verbinden Ihr lokales Netzwerk mit der Microsoft-Cloud, indem Sie einen Verbindungsanbieter anstelle des öffentlichen Internets verwenden.</span><span class="sxs-lookup"><span data-stu-id="af80c-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="af80c-108">Der Besitzer eines Express Route-Schaltkreises kann bis zu 10 Berechtigungen für jeden Schaltkreis erstellen. Diese Berechtigungen generieren einen Autorisierungsschlüssel, der von einem virtuellen Netzwerk Besitzer verwendet werden kann, um sein Netzwerk mit dem Schaltkreis (eine Autorisierung pro virtuelles Netzwerk) zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="af80c-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="af80c-109">**Add-AzureRmExpressRouteCircuitAuthorization** fügt eine neue Autorisierung zu einem Schaltkreis hinzu und generiert gleichzeitig den entsprechenden Autorisierungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="af80c-109">**Add-AzureRmExpressRouteCircuitAuthorization** adds a new authorization to a circuit and, at the same time, generates the corresponding authorization key.</span></span> <span data-ttu-id="af80c-110">Diese Schlüssel können jederzeit angezeigt werden, indem Sie das Get-AzureRmExpressRouteCircuitAuthorization-Cmdlet ausführen und es nach Bedarf dann kopieren und an den entsprechenden Netzwerk Besitzer weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="af80c-110">These keys can be viewed at any time by running the Get-AzureRmExpressRouteCircuitAuthorization cmdlet and, as needed, can then be copied and forwarded to the appropriate network owner.</span></span>

<span data-ttu-id="af80c-111">Beachten Sie, dass Sie nach dem Ausführen von **Add-AzureRmExpressRouteCircuitAuthorization** das Set-AzureRmExpressRouteCircuit-Cmdlet aufrufen müssen, um den Schlüssel zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="af80c-111">Note that, after running **Add-AzureRmExpressRouteCircuitAuthorization** , you must call the Set-AzureRmExpressRouteCircuit cmdlet to activate the key.</span></span> <span data-ttu-id="af80c-112">Wenn Sie " **Satz-AzureRmExpressRouteCircuit** " nicht aufrufen, wird die Autorisierung dem Schaltkreis hinzugefügt, aber nicht für die Verwendung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="af80c-112">If you do not call **Set-AzureRmExpressRouteCircuit** the authorization will be added to the circuit but will not be enabled for use.</span></span>

## <span data-ttu-id="af80c-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="af80c-113">EXAMPLES</span></span>

### <span data-ttu-id="af80c-114">Beispiel 1: Hinzufügen einer Autorisierung zum angegebenen Express Route-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="af80c-114">Example 1: Add an authorization to the specified ExpressRoute circuit</span></span>
```
$Circuit = Get-AzureRmExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzureRmExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="af80c-115">Mit den Befehlen in diesem Beispiel wird eine neue Autorisierung zu einem vorhandenen Express Route-Schaltkreis hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="af80c-115">The commands in this example add a new authorization to an existing ExpressRoute circuit.</span></span> <span data-ttu-id="af80c-116">Der erste Befehl verwendet **Get-AzureRmExpressRouteCircuit** , um einen Objektverweis auf einen Schaltkreis mit dem Namen ContosoCircuit zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="af80c-116">The first command uses **Get-AzureRmExpressRouteCircuit** to create an object reference to a circuit named ContosoCircuit.</span></span> <span data-ttu-id="af80c-117">Dieser Objektverweis wird in einer Variablen mit dem Namen $Circuit gespeichert.</span><span class="sxs-lookup"><span data-stu-id="af80c-117">That object reference is stored in a variable named $Circuit.</span></span>

<span data-ttu-id="af80c-118">Im zweiten Befehl wird das Cmdlet **Add-AzureRmExpressRouteCircuitAuthorization** verwendet, um dem Express Route-Schaltkreis eine neue Autorisierung (ContosoCircuitAuthorization) hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="af80c-118">In the second command, the **Add-AzureRmExpressRouteCircuitAuthorization** cmdlet is used to add a new authorization (ContosoCircuitAuthorization) to the ExpressRoute circuit.</span></span> <span data-ttu-id="af80c-119">Mit diesem Befehl wird die Autorisierung hinzugefügt, diese Autorisierung wird jedoch nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="af80c-119">This command adds the authorization but does not activate that authorization.</span></span> <span data-ttu-id="af80c-120">Für das Aktivieren einer Autorisierung ist die im letzten Befehl im Beispiel angezeigte **Satz-AzureRmExpressRouteCircuit** erforderlich.</span><span class="sxs-lookup"><span data-stu-id="af80c-120">Activating an authorization requires the **Set-AzureRmExpressRouteCircuit** shown in the final command in the example.</span></span>

## <span data-ttu-id="af80c-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="af80c-121">PARAMETERS</span></span>

### <span data-ttu-id="af80c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af80c-122">-DefaultProfile</span></span>
<span data-ttu-id="af80c-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="af80c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af80c-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="af80c-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="af80c-125">Gibt den Express Route-Schaltkreis an, dem dieses Cmdlet die Autorisierung hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="af80c-125">Specifies the ExpressRoute circuit that this cmdlet adds the authorization to.</span></span>

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

### <span data-ttu-id="af80c-126">-Name</span><span class="sxs-lookup"><span data-stu-id="af80c-126">-Name</span></span>
<span data-ttu-id="af80c-127">Gibt den Namen der Schaltkreis Autorisierung an, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="af80c-127">Specifies the name of the circuit authorization to be added.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af80c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af80c-128">CommonParameters</span></span>
<span data-ttu-id="af80c-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af80c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af80c-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af80c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af80c-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="af80c-131">INPUTS</span></span>

### <span data-ttu-id="af80c-132">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="af80c-132">PSExpressRouteCircuit</span></span>
<span data-ttu-id="af80c-133">**Add-AzureRmExpressRouteCircuitAuthorization** akzeptiert Pipelineinstanzen des **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="af80c-133">**Add-AzureRmExpressRouteCircuitAuthorization** accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="af80c-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="af80c-134">OUTPUTS</span></span>

### <span data-ttu-id="af80c-135">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="af80c-135">PSExpressRouteCircuit</span></span>
<span data-ttu-id="af80c-136">**Add-AzureRmExpressRouteCircuitAuthorization** ändert Instanzen des **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="af80c-136">**Add-AzureRmExpressRouteCircuitAuthorization** modifies instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="af80c-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="af80c-137">NOTES</span></span>

## <span data-ttu-id="af80c-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="af80c-138">RELATED LINKS</span></span>

[<span data-ttu-id="af80c-139">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="af80c-139">Get-AzureRmExpressRouteCircuit</span></span>](./Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="af80c-140">Get-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="af80c-140">Get-AzureRmExpressRouteCircuitAuthorization</span></span>](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="af80c-141">Neu – AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="af80c-141">New-AzureRmExpressRouteCircuitAuthorization</span></span>](./New-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="af80c-142">Remove-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="af80c-142">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>](./Remove-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="af80c-143">Satz-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="af80c-143">Set-AzureRmExpressRouteCircuit</span></span>](./Set-AzureRmExpressRouteCircuit.md)
