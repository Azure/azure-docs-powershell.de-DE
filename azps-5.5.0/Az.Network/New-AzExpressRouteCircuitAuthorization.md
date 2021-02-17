---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 28b45f5368fb7a63450276c054654313d7e1c517
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156924"
---
# <span data-ttu-id="61b84-101">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="61b84-101">New-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="61b84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61b84-102">SYNOPSIS</span></span>
<span data-ttu-id="61b84-103">Erstellt eine ExpressRoute-Schaltkreisautorisierung.</span><span class="sxs-lookup"><span data-stu-id="61b84-103">Creates an ExpressRoute circuit authorization.</span></span>

## <span data-ttu-id="61b84-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="61b84-104">SYNTAX</span></span>

```
New-AzExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="61b84-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="61b84-105">DESCRIPTION</span></span>
<span data-ttu-id="61b84-106">Das **Cmdlet "New-AzExpressRouteCircuitAuthorization"** erstellt eine Schaltkreisautorisierung, die einem Leitungen hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="61b84-106">The **New-AzExpressRouteCircuitAuthorization** cmdlet creates a circuit authorization that can be added to an ExpressRoute circuit.</span></span> <span data-ttu-id="61b84-107">ExpressRoute-Schaltkreise verbinden Ihr lokales Netzwerk mit der Microsoft-Cloud, indem anstelle des öffentlichen Internets ein Konnektivitätsanbieter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="61b84-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="61b84-108">Der Besitzer eines #A0 kann bis zu 10 Autorisierungen für jeden Schaltkreis erstellen. diese Autorisierungen generieren einen Autorisierungsschlüssel, der von einem virtuellen Netzwerkbesitzer verwendet werden kann, um ein Netzwerk mit dem Schaltkreis zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="61b84-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect a network to the circuit.</span></span> <span data-ttu-id="61b84-109">Pro virtuellem Netzwerk kann es nur eine Autorisierung gibt.</span><span class="sxs-lookup"><span data-stu-id="61b84-109">There can only one authorization per virtual network.</span></span>
<span data-ttu-id="61b84-110">Nachdem Sie einen "ExpressRoute"-Schaltkreis erstellt haben, können Sie **"Add-AzExpressRouteCircuitAuthorization"** verwenden, um dem Schaltkreis eine Autorisierung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="61b84-110">After you create an ExpressRoute circuit you can use **Add-AzExpressRouteCircuitAuthorization** to add an authorization to that circuit.</span></span>
<span data-ttu-id="61b84-111">Alternativ können Sie **"New-AzExpressRouteCircuitAuthorization"** verwenden, um eine Autorisierung zu erstellen, die gleichzeitig mit der Erstellung des Schaltkreises einem neuen Schaltkreis hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="61b84-111">Alternatively, you can use **New-AzExpressRouteCircuitAuthorization** to create an authorization that can be added to a new circuit at the same time the circuit is created.</span></span>

## <span data-ttu-id="61b84-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="61b84-112">EXAMPLES</span></span>

### <span data-ttu-id="61b84-113">Beispiel 1: Erstellen einer Neuen Schaltkreisautorisierung</span><span class="sxs-lookup"><span data-stu-id="61b84-113">Example 1: Create a new circuit authorization</span></span>
```
$Authorization = New-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

<span data-ttu-id="61b84-114">Mit diesem Befehl wird eine neue Schaltkreisautorisierung namens "ContosoCircuitAuthorization" erstellt und dieses Objekt dann in einer Variablen namens "$Authorization.</span><span class="sxs-lookup"><span data-stu-id="61b84-114">This command creates a new circuit authorization named ContosoCircuitAuthorization and then stores that object in a variable named $Authorization.</span></span> <span data-ttu-id="61b84-115">Das Speichern des Objekts in einer Variablen ist wichtig: Obwohl **"New-AzExpressRouteCircuitAuthorization"** eine Schaltkreisautorisierung erstellen kann, kann diese Autorisierung einer Schaltkreisroute nicht hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="61b84-115">Saving the object to a variable is important: although **New-AzExpressRouteCircuitAuthorization** can create a circuit authorization it cannot add that authorization to a circuit route.</span></span> <span data-ttu-id="61b84-116">Stattdessen wird die variable $Authorization beim New-AzExpressRouteCircuit erstellen eines völlig neuen "ExpressRoute"-Schaltkreises verwendet.</span><span class="sxs-lookup"><span data-stu-id="61b84-116">Instead, the variable $Authorization is used New-AzExpressRouteCircuit when creating a brand-new ExpressRoute circuit.</span></span>
<span data-ttu-id="61b84-117">Weitere Informationen finden Sie in der Dokumentation zum New-AzExpressRouteCircuit Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61b84-117">For more information, see the documentation for the New-AzExpressRouteCircuit cmdlet.</span></span>

## <span data-ttu-id="61b84-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61b84-118">PARAMETERS</span></span>

### <span data-ttu-id="61b84-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61b84-119">-DefaultProfile</span></span>
<span data-ttu-id="61b84-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="61b84-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61b84-121">-Name</span><span class="sxs-lookup"><span data-stu-id="61b84-121">-Name</span></span>
<span data-ttu-id="61b84-122">Gibt einen eindeutigen Namen für die neue ExpressRoute-Schaltkreisautorisierung an.</span><span class="sxs-lookup"><span data-stu-id="61b84-122">Specifies a unique name for the new ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="61b84-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61b84-123">CommonParameters</span></span>
<span data-ttu-id="61b84-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61b84-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61b84-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61b84-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61b84-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="61b84-126">INPUTS</span></span>

### <span data-ttu-id="61b84-127">Keine</span><span class="sxs-lookup"><span data-stu-id="61b84-127">None</span></span>

## <span data-ttu-id="61b84-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="61b84-128">OUTPUTS</span></span>

### <span data-ttu-id="61b84-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="61b84-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="61b84-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="61b84-130">NOTES</span></span>

## <span data-ttu-id="61b84-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="61b84-131">RELATED LINKS</span></span>

[<span data-ttu-id="61b84-132">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="61b84-132">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="61b84-133">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="61b84-133">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="61b84-134">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="61b84-134">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)

