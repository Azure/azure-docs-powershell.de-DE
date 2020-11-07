---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9994E2B2-20A1-4E95-9A9F-379B8B63F7F5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: efe2a149d2ca02c075b2e0a1f73191e9e2b8859b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841840"
---
# <span data-ttu-id="5ee77-101">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="5ee77-101">Add-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="5ee77-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5ee77-102">SYNOPSIS</span></span>
<span data-ttu-id="5ee77-103">Fügt eine Express Route-Schaltkreis Autorisierung hinzu.</span><span class="sxs-lookup"><span data-stu-id="5ee77-103">Adds an ExpressRoute circuit authorization.</span></span>

## <span data-ttu-id="5ee77-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ee77-104">SYNTAX</span></span>

```
Add-AzExpressRouteCircuitAuthorization -Name <String> -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ee77-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5ee77-105">DESCRIPTION</span></span>
<span data-ttu-id="5ee77-106">Mit dem Cmdlet **Add-AzExpressRouteCircuitAuthorization** wird eine Autorisierung zu einem Express Route-Schaltkreis hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5ee77-106">The **Add-AzExpressRouteCircuitAuthorization** cmdlet adds an authorization to an ExpressRoute circuit.</span></span> <span data-ttu-id="5ee77-107">Express Route-Schaltkreise verbinden Ihr lokales Netzwerk mit der Microsoft-Cloud, indem Sie einen Verbindungsanbieter anstelle des öffentlichen Internets verwenden.</span><span class="sxs-lookup"><span data-stu-id="5ee77-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="5ee77-108">Der Besitzer eines Express Route-Schaltkreises kann bis zu 10 Berechtigungen für jeden Schaltkreis erstellen. Diese Berechtigungen generieren einen Autorisierungsschlüssel, der von einem virtuellen Netzwerk Besitzer verwendet werden kann, um sein Netzwerk mit dem Schaltkreis (eine Autorisierung pro virtuelles Netzwerk) zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="5ee77-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="5ee77-109">**Add-AzExpressRouteCircuitAuthorization** fügt eine neue Autorisierung zu einem Schaltkreis hinzu und generiert gleichzeitig den entsprechenden Autorisierungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="5ee77-109">**Add-AzExpressRouteCircuitAuthorization** adds a new authorization to a circuit and, at the same time, generates the corresponding authorization key.</span></span> <span data-ttu-id="5ee77-110">Diese Schlüssel können jederzeit angezeigt werden, indem Sie das Get-AzExpressRouteCircuitAuthorization-Cmdlet ausführen und es nach Bedarf dann kopieren und an den entsprechenden Netzwerk Besitzer weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="5ee77-110">These keys can be viewed at any time by running the Get-AzExpressRouteCircuitAuthorization cmdlet and, as needed, can then be copied and forwarded to the appropriate network owner.</span></span>

<span data-ttu-id="5ee77-111">Beachten Sie, dass Sie nach dem Ausführen von **Add-AzExpressRouteCircuitAuthorization** das Set-AzExpressRouteCircuit-Cmdlet aufrufen müssen, um den Schlüssel zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="5ee77-111">Note that, after running **Add-AzExpressRouteCircuitAuthorization** , you must call the Set-AzExpressRouteCircuit cmdlet to activate the key.</span></span> <span data-ttu-id="5ee77-112">Wenn Sie " **Satz-AzExpressRouteCircuit** " nicht aufrufen, wird die Autorisierung dem Schaltkreis hinzugefügt, aber nicht für die Verwendung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="5ee77-112">If you do not call **Set-AzExpressRouteCircuit** the authorization will be added to the circuit but will not be enabled for use.</span></span>

## <span data-ttu-id="5ee77-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5ee77-113">EXAMPLES</span></span>

### <span data-ttu-id="5ee77-114">Beispiel 1: Hinzufügen einer Autorisierung zum angegebenen Express Route-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="5ee77-114">Example 1: Add an authorization to the specified ExpressRoute circuit</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Add-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization" -Circuit $Circuit
Set-AzExpressRouteCircuit -ExpressRouteCircuit $Circuit
```

<span data-ttu-id="5ee77-115">Mit den Befehlen in diesem Beispiel wird eine neue Autorisierung zu einem vorhandenen Express Route-Schaltkreis hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5ee77-115">The commands in this example add a new authorization to an existing ExpressRoute circuit.</span></span> <span data-ttu-id="5ee77-116">Der erste Befehl verwendet **Get-AzExpressRouteCircuit** , um einen Objektverweis auf einen Schaltkreis mit dem Namen ContosoCircuit zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5ee77-116">The first command uses **Get-AzExpressRouteCircuit** to create an object reference to a circuit named ContosoCircuit.</span></span> <span data-ttu-id="5ee77-117">Dieser Objektverweis wird in einer Variablen mit dem Namen $Circuit gespeichert.</span><span class="sxs-lookup"><span data-stu-id="5ee77-117">That object reference is stored in a variable named $Circuit.</span></span>

<span data-ttu-id="5ee77-118">Im zweiten Befehl wird das Cmdlet **Add-AzExpressRouteCircuitAuthorization** verwendet, um dem Express Route-Schaltkreis eine neue Autorisierung (ContosoCircuitAuthorization) hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="5ee77-118">In the second command, the **Add-AzExpressRouteCircuitAuthorization** cmdlet is used to add a new authorization (ContosoCircuitAuthorization) to the ExpressRoute circuit.</span></span> <span data-ttu-id="5ee77-119">Mit diesem Befehl wird die Autorisierung hinzugefügt, diese Autorisierung wird jedoch nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="5ee77-119">This command adds the authorization but does not activate that authorization.</span></span> <span data-ttu-id="5ee77-120">Für das Aktivieren einer Autorisierung ist die im letzten Befehl im Beispiel angezeigte **Satz-AzExpressRouteCircuit** erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5ee77-120">Activating an authorization requires the **Set-AzExpressRouteCircuit** shown in the final command in the example.</span></span>

## <span data-ttu-id="5ee77-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ee77-121">PARAMETERS</span></span>

### <span data-ttu-id="5ee77-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ee77-122">-DefaultProfile</span></span>
<span data-ttu-id="5ee77-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5ee77-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ee77-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5ee77-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="5ee77-125">Gibt den Express Route-Schaltkreis an, dem dieses Cmdlet die Autorisierung hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="5ee77-125">Specifies the ExpressRoute circuit that this cmdlet adds the authorization to.</span></span>

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

### <span data-ttu-id="5ee77-126">-Name</span><span class="sxs-lookup"><span data-stu-id="5ee77-126">-Name</span></span>
<span data-ttu-id="5ee77-127">Gibt den Namen der Schaltkreis Autorisierung an, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5ee77-127">Specifies the name of the circuit authorization to be added.</span></span>

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

### <span data-ttu-id="5ee77-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ee77-128">CommonParameters</span></span>
<span data-ttu-id="5ee77-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ee77-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ee77-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ee77-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ee77-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5ee77-131">INPUTS</span></span>

### <span data-ttu-id="5ee77-132">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5ee77-132">PSExpressRouteCircuit</span></span>
<span data-ttu-id="5ee77-133">**Add-AzExpressRouteCircuitAuthorization** akzeptiert Pipelineinstanzen des **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="5ee77-133">**Add-AzExpressRouteCircuitAuthorization** accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="5ee77-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5ee77-134">OUTPUTS</span></span>

### <span data-ttu-id="5ee77-135">PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5ee77-135">PSExpressRouteCircuit</span></span>
<span data-ttu-id="5ee77-136">**Add-AzExpressRouteCircuitAuthorization** ändert Instanzen des **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="5ee77-136">**Add-AzExpressRouteCircuitAuthorization** modifies instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit** object.</span></span>

## <span data-ttu-id="5ee77-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="5ee77-137">NOTES</span></span>

## <span data-ttu-id="5ee77-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5ee77-138">RELATED LINKS</span></span>

[<span data-ttu-id="5ee77-139">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5ee77-139">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="5ee77-140">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="5ee77-140">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="5ee77-141">Neu – AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="5ee77-141">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="5ee77-142">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="5ee77-142">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="5ee77-143">Satz-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="5ee77-143">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
