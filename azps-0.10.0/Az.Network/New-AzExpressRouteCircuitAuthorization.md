---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 0f17d30b6f47effab5b0039bd56172cbe580392c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841364"
---
# <span data-ttu-id="3a58a-101">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="3a58a-101">New-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="3a58a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3a58a-102">SYNOPSIS</span></span>
<span data-ttu-id="3a58a-103">Erstellt eine Express Route-Schaltkreis Autorisierung.</span><span class="sxs-lookup"><span data-stu-id="3a58a-103">Creates an ExpressRoute circuit authorization.</span></span>

## <span data-ttu-id="3a58a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a58a-104">SYNTAX</span></span>

```
New-AzExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3a58a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3a58a-105">DESCRIPTION</span></span>
<span data-ttu-id="3a58a-106">Das Cmdlet **New-AzExpressRouteCircuitAuthorization** erstellt eine Schaltkreis Autorisierung, die einem Express Route-Schaltkreis hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="3a58a-106">The **New-AzExpressRouteCircuitAuthorization** cmdlet creates a circuit authorization that can be added to an ExpressRoute circuit.</span></span> <span data-ttu-id="3a58a-107">Express Route-Schaltkreise verbinden Ihr lokales Netzwerk mit der Microsoft-Cloud, indem Sie einen Verbindungsanbieter anstelle des öffentlichen Internets verwenden.</span><span class="sxs-lookup"><span data-stu-id="3a58a-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="3a58a-108">Der Besitzer eines Express Route-Schaltkreises kann bis zu 10 Berechtigungen für jeden Schaltkreis erstellen. Diese Berechtigungen generieren einen Autorisierungsschlüssel, der von einem virtuellen Netzwerk Besitzer verwendet werden kann, um ein Netzwerk mit dem Schaltkreis zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="3a58a-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect a network to the circuit.</span></span> <span data-ttu-id="3a58a-109">Pro virtuelles Netzwerk kann nur eine Autorisierung vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="3a58a-109">There can only one authorization per virtual network.</span></span>

<span data-ttu-id="3a58a-110">Nachdem Sie einen Express Route-Schaltkreis erstellt haben, können Sie **Add-AzExpressRouteCircuitAuthorization** verwenden, um dieser Schaltkreis eine Autorisierung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="3a58a-110">After you create an ExpressRoute circuit you can use **Add-AzExpressRouteCircuitAuthorization** to add an authorization to that circuit.</span></span>
<span data-ttu-id="3a58a-111">Alternativ können Sie auch **New-AzExpressRouteCircuitAuthorization** verwenden, um eine Autorisierung zu erstellen, die gleichzeitig zu einem neuen Schaltkreis hinzugefügt werden kann, wenn der Schaltkreis erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="3a58a-111">Alternatively, you can use **New-AzExpressRouteCircuitAuthorization** to create an authorization that can be added to a new circuit at the same time the circuit is created.</span></span>

## <span data-ttu-id="3a58a-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3a58a-112">EXAMPLES</span></span>

### <span data-ttu-id="3a58a-113">Beispiel 1: Erstellen einer neuen Schaltkreis Autorisierung</span><span class="sxs-lookup"><span data-stu-id="3a58a-113">Example 1: Create a new circuit authorization</span></span>
```
$Authorization = New-AzExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

<span data-ttu-id="3a58a-114">Dieser Befehl erstellt eine neue Schaltkreis Autorisierung mit dem Namen "ContosoCircuitAuthorization" und speichert dieses Objekt dann in einer Variablen mit dem Namen "$Authorization".</span><span class="sxs-lookup"><span data-stu-id="3a58a-114">This command creates a new circuit authorization named ContosoCircuitAuthorization and then stores that object in a variable named $Authorization.</span></span> <span data-ttu-id="3a58a-115">Das Speichern des Objekts in einer Variablen ist wichtig: Obwohl **New-AzExpressRouteCircuitAuthorization** eine Schaltkreis Autorisierung erstellen kann, kann diese Berechtigung nicht zu einer leitungsroute hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="3a58a-115">Saving the object to a variable is important: although **New-AzExpressRouteCircuitAuthorization** can create a circuit authorization it cannot add that authorization to a circuit route.</span></span> <span data-ttu-id="3a58a-116">Stattdessen wird die Variable $Authorization New-AzExpressRouteCircuit beim Erstellen eines brandneuen Express Route-Schaltkreises verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a58a-116">Instead, the variable $Authorization is used New-AzExpressRouteCircuit when creating a brand-new ExpressRoute circuit.</span></span>

<span data-ttu-id="3a58a-117">Weitere Informationen finden Sie in der Dokumentation zum New-AzExpressRouteCircuit-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a58a-117">For more information, see the documentation for the New-AzExpressRouteCircuit cmdlet.</span></span>

## <span data-ttu-id="3a58a-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a58a-118">PARAMETERS</span></span>

### <span data-ttu-id="3a58a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a58a-119">-DefaultProfile</span></span>
<span data-ttu-id="3a58a-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3a58a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a58a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3a58a-121">-Name</span></span>
<span data-ttu-id="3a58a-122">Gibt einen eindeutigen Namen für die neue Express Route-Schaltkreis Autorisierung an.</span><span class="sxs-lookup"><span data-stu-id="3a58a-122">Specifies a unique name for the new ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="3a58a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a58a-123">CommonParameters</span></span>
<span data-ttu-id="3a58a-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a58a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a58a-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a58a-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a58a-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3a58a-126">INPUTS</span></span>

### <span data-ttu-id="3a58a-127">Keine</span><span class="sxs-lookup"><span data-stu-id="3a58a-127">None</span></span>
<span data-ttu-id="3a58a-128">Dieses Cmdlet akzeptiert keine Pipeline-Eingabe.</span><span class="sxs-lookup"><span data-stu-id="3a58a-128">This cmdlet does not accept pipelined input.</span></span>

## <span data-ttu-id="3a58a-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3a58a-129">OUTPUTS</span></span>

### <span data-ttu-id="3a58a-130">PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="3a58a-130">PSExpressRouteCircuitAuthorization</span></span>
<span data-ttu-id="3a58a-131">Dieses Cmdlet erstellt Instanzen des **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitAuthorization** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="3a58a-131">This cmdlet creates instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization** object.</span></span>

## <span data-ttu-id="3a58a-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="3a58a-132">NOTES</span></span>

## <span data-ttu-id="3a58a-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3a58a-133">RELATED LINKS</span></span>

[<span data-ttu-id="3a58a-134">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="3a58a-134">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="3a58a-135">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="3a58a-135">Get-AzExpressRouteCircuitAuthorization</span></span>](./Get-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="3a58a-136">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="3a58a-136">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)

