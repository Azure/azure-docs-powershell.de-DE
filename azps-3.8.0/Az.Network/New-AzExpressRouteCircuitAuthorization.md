---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 28b45f5368fb7a63450276c054654313d7e1c517
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004954"
---
# <span data-ttu-id="80ffe-101">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="80ffe-101">New-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="80ffe-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="80ffe-102">SYNOPSIS</span></span>
<span data-ttu-id="80ffe-103">Erstellt eine Express Route-Schaltkreis Autorisierung.</span><span class="sxs-lookup"><span data-stu-id="80ffe-103">Creates an ExpressRoute circuit authorization.</span></span>

## <span data-ttu-id="80ffe-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="80ffe-104">SYNTAX</span></span>

```
New-AzExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="80ffe-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="80ffe-105">DESCRIPTION</span></span>
<span data-ttu-id="80ffe-106">Das Cmdlet **New-AzExpressRouteCircuitAuthorization** erstellt eine Schaltkreis Autorisierung, die einem Express Route-Schaltkreis hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="80ffe-106">The **New-AzExpressRouteCircuitAuthorization** cmdlet creates a circuit authorization that can be added to an ExpressRoute circuit.</span></span> <span data-ttu-id="80ffe-107">Express Route-Schaltkreise verbinden Ihr lokales Netzwerk mit der Microsoft-Cloud, indem Sie einen Verbindungsanbieter anstelle des öffentlichen Internets verwenden.</span><span class="sxs-lookup"><span data-stu-id="80ffe-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="80ffe-108">Der Besitzer eines Express Route-Schaltkreises kann bis zu 10 Berechtigungen für jeden Schaltkreis erstellen. Diese Berechtigungen generieren einen Autorisierungsschlüssel, der von einem virtuellen Netzwerk Besitzer verwendet werden kann, um ein Netzwerk mit dem Schaltkreis zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="80ffe-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect a network to the circuit.</span></span> <span data-ttu-id="80ffe-109">Pro virtuelles Netzwerk kann nur eine Autorisierung vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="80ffe-109">There can only one authorization per virtual network.</span></span>
<span data-ttu-id="80ffe-110">Nachdem Sie einen Express Route-Schaltkreis erstellt haben, können Sie **Add-AzExpressRouteCircuitAuthorization** verwenden, um dieser Schaltkreis eine Autorisierung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="80ffe-110">After you create an ExpressRoute circuit you can use **Add-AzExpressRouteCircuitAuthorization** to add an authorization to that circuit.</span></span>
<span data-ttu-id="80ffe-111">Alternativ können Sie auch **New-AzExpressRouteCircuitAuthorization** verwenden, um eine Autorisierung zu erstellen, die gleichzeitig zu einem neuen Schaltkreis hinzugefügt werden kann, wenn der Schaltkreis erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="80ffe-111">Alternatively, you can use **New-AzExpressRouteCircuitAuthorization** to create an authorization that can be added to a new circuit at the same time the circuit is created.</span></span>

## <span data-ttu-id="80ffe-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="80ffe-112">EXAMPLES</span></span>

### <span data-ttu-id="80ffe-113">Beispiel 1: Erstellen einer neuen Schaltkreis Autorisierung</span><span class="sxs-lookup"><span data-stu-id="80ffe-113">Example 1: Create a new circuit authorization</span></span>
```
$Authorization = New-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

<span data-ttu-id="80ffe-114">Dieser Befehl erstellt eine neue Schaltkreis Autorisierung mit dem Namen "ContosoCircuitAuthorization" und speichert dieses Objekt dann in einer Variablen mit dem Namen "$Authorization".</span><span class="sxs-lookup"><span data-stu-id="80ffe-114">This command creates a new circuit authorization named ContosoCircuitAuthorization and then stores that object in a variable named $Authorization.</span></span> <span data-ttu-id="80ffe-115">Das Speichern des Objekts in einer Variablen ist wichtig: Obwohl **New-AzExpressRouteCircuitAuthorization** eine Schaltkreis Autorisierung erstellen kann, kann diese Berechtigung nicht zu einer leitungsroute hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="80ffe-115">Saving the object to a variable is important: although **New-AzExpressRouteCircuitAuthorization** can create a circuit authorization it cannot add that authorization to a circuit route.</span></span> <span data-ttu-id="80ffe-116">Stattdessen wird die Variable $Authorization New-AzExpressRouteCircuit beim Erstellen eines brandneuen Express Route-Schaltkreises verwendet.</span><span class="sxs-lookup"><span data-stu-id="80ffe-116">Instead, the variable $Authorization is used New-AzExpressRouteCircuit when creating a brand-new ExpressRoute circuit.</span></span>
<span data-ttu-id="80ffe-117">Weitere Informationen finden Sie in der Dokumentation zum New-AzExpressRouteCircuit-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80ffe-117">For more information, see the documentation for the New-AzExpressRouteCircuit cmdlet.</span></span>

## <span data-ttu-id="80ffe-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="80ffe-118">PARAMETERS</span></span>

### <span data-ttu-id="80ffe-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80ffe-119">-DefaultProfile</span></span>
<span data-ttu-id="80ffe-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="80ffe-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80ffe-121">-Name</span><span class="sxs-lookup"><span data-stu-id="80ffe-121">-Name</span></span>
<span data-ttu-id="80ffe-122">Gibt einen eindeutigen Namen für die neue Express Route-Schaltkreis Autorisierung an.</span><span class="sxs-lookup"><span data-stu-id="80ffe-122">Specifies a unique name for the new ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="80ffe-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80ffe-123">CommonParameters</span></span>
<span data-ttu-id="80ffe-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80ffe-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80ffe-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80ffe-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80ffe-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="80ffe-126">INPUTS</span></span>

### <span data-ttu-id="80ffe-127">Keine</span><span class="sxs-lookup"><span data-stu-id="80ffe-127">None</span></span>

## <span data-ttu-id="80ffe-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="80ffe-128">OUTPUTS</span></span>

### <span data-ttu-id="80ffe-129">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="80ffe-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="80ffe-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="80ffe-130">NOTES</span></span>

## <span data-ttu-id="80ffe-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="80ffe-131">RELATED LINKS</span></span>

[<span data-ttu-id="80ffe-132">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="80ffe-132">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="80ffe-133">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="80ffe-133">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="80ffe-134">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="80ffe-134">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)

