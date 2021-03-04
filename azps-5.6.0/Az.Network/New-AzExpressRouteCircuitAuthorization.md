---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/powershell/module/az.network/new-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 9c247784a9f890d97aee301383656f97ef9c7dd4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941080"
---
# <span data-ttu-id="efb72-101">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="efb72-101">New-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="efb72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efb72-102">SYNOPSIS</span></span>
<span data-ttu-id="efb72-103">Erstellt eine ExpressRoute-Schaltkreisautorisierung.</span><span class="sxs-lookup"><span data-stu-id="efb72-103">Creates an ExpressRoute circuit authorization.</span></span>

## <span data-ttu-id="efb72-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="efb72-104">SYNTAX</span></span>

```
New-AzExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="efb72-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="efb72-105">DESCRIPTION</span></span>
<span data-ttu-id="efb72-106">Das **Cmdlet New-AzExpressRouteCircuitAuthorization** erstellt eine Schaltungsautorisierung, die einem ExpressRoute-Schaltkreis hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="efb72-106">The **New-AzExpressRouteCircuitAuthorization** cmdlet creates a circuit authorization that can be added to an ExpressRoute circuit.</span></span> <span data-ttu-id="efb72-107">ExpressRoute-Schaltkreise verbinden Ihr lokales Netzwerk mit der Microsoft-Cloud, indem sie einen Konnektivitätsanbieter anstelle des öffentlichen Internets verwenden.</span><span class="sxs-lookup"><span data-stu-id="efb72-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="efb72-108">Der Besitzer eines #A0 kann bis zu 10 Berechtigungen für jeden Schaltkreis erstellen. Diese Autorisierungen generieren einen Autorisierungsschlüssel, der von einem Besitzer eines virtuellen Netzwerks verwendet werden kann, um ein Netzwerk mit dem Schaltkreis zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="efb72-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect a network to the circuit.</span></span> <span data-ttu-id="efb72-109">Pro virtuellem Netzwerk kann nur eine Autorisierung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="efb72-109">There can only one authorization per virtual network.</span></span>
<span data-ttu-id="efb72-110">Nachdem Sie einen ExpressRoute-Schaltkreis erstellt haben, können Sie **Add-AzExpressRouteCircuitAuthorization** verwenden, um dieser Schaltung eine Autorisierung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="efb72-110">After you create an ExpressRoute circuit you can use **Add-AzExpressRouteCircuitAuthorization** to add an authorization to that circuit.</span></span>
<span data-ttu-id="efb72-111">Alternativ können Sie **new-AzExpressRouteCircuitAuthorization** verwenden, um eine Autorisierung zu erstellen, die gleichzeitig mit der Erstellung des Schaltkreises einem neuen Schaltkreis hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="efb72-111">Alternatively, you can use **New-AzExpressRouteCircuitAuthorization** to create an authorization that can be added to a new circuit at the same time the circuit is created.</span></span>

## <span data-ttu-id="efb72-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="efb72-112">EXAMPLES</span></span>

### <span data-ttu-id="efb72-113">Beispiel 1: Erstellen einer neuen Schaltkreisautorisierung</span><span class="sxs-lookup"><span data-stu-id="efb72-113">Example 1: Create a new circuit authorization</span></span>
```
$Authorization = New-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

<span data-ttu-id="efb72-114">Dieser Befehl erstellt eine neue Schaltkreisautorisierung namens ContosoCircuitAuthorization und speichert dieses Objekt dann in einer Variablen namens $Authorization.</span><span class="sxs-lookup"><span data-stu-id="efb72-114">This command creates a new circuit authorization named ContosoCircuitAuthorization and then stores that object in a variable named $Authorization.</span></span> <span data-ttu-id="efb72-115">Das Speichern des Objekts in einer Variablen ist wichtig: Obwohl **New-AzExpressRouteCircuitAuthorization** eine Schaltungsautorisierung erstellen kann, kann diese Autorisierung nicht zu einer Stromkreisroute hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="efb72-115">Saving the object to a variable is important: although **New-AzExpressRouteCircuitAuthorization** can create a circuit authorization it cannot add that authorization to a circuit route.</span></span> <span data-ttu-id="efb72-116">Stattdessen wird die Variable $Authorization verwendet, New-AzExpressRouteCircuit beim Erstellen eines brandneuen ExpressRoute-Schaltkreises verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="efb72-116">Instead, the variable $Authorization is used New-AzExpressRouteCircuit when creating a brand-new ExpressRoute circuit.</span></span>
<span data-ttu-id="efb72-117">Weitere Informationen finden Sie in der Dokumentation zum New-AzExpressRouteCircuit Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efb72-117">For more information, see the documentation for the New-AzExpressRouteCircuit cmdlet.</span></span>

## <span data-ttu-id="efb72-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="efb72-118">PARAMETERS</span></span>

### <span data-ttu-id="efb72-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efb72-119">-DefaultProfile</span></span>
<span data-ttu-id="efb72-120">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="efb72-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efb72-121">-Name</span><span class="sxs-lookup"><span data-stu-id="efb72-121">-Name</span></span>
<span data-ttu-id="efb72-122">Gibt einen eindeutigen Namen für die neue ExpressRoute-Schaltungsautorisierung an.</span><span class="sxs-lookup"><span data-stu-id="efb72-122">Specifies a unique name for the new ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="efb72-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efb72-123">CommonParameters</span></span>
<span data-ttu-id="efb72-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efb72-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efb72-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efb72-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efb72-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="efb72-126">INPUTS</span></span>

### <span data-ttu-id="efb72-127">Keine</span><span class="sxs-lookup"><span data-stu-id="efb72-127">None</span></span>

## <span data-ttu-id="efb72-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="efb72-128">OUTPUTS</span></span>

### <span data-ttu-id="efb72-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="efb72-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="efb72-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="efb72-130">NOTES</span></span>

## <span data-ttu-id="efb72-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="efb72-131">RELATED LINKS</span></span>

[<span data-ttu-id="efb72-132">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="efb72-132">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="efb72-133">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="efb72-133">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="efb72-134">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="efb72-134">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)

