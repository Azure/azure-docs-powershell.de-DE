---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B6E55944-1B78-463F-9FC9-98097FEEC278
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 68599a48c4b0e608f629a628968c1918e62ec226
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "93506022"
---
# <span data-ttu-id="35c5d-101">New-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="35c5d-101">New-AzureRmExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="35c5d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="35c5d-102">SYNOPSIS</span></span>
<span data-ttu-id="35c5d-103">Erstellt eine Express Route-Schaltkreis Autorisierung.</span><span class="sxs-lookup"><span data-stu-id="35c5d-103">Creates an ExpressRoute circuit authorization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35c5d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="35c5d-104">SYNTAX</span></span>

```
New-AzureRmExpressRouteCircuitAuthorization -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="35c5d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="35c5d-105">DESCRIPTION</span></span>
<span data-ttu-id="35c5d-106">Das Cmdlet **New-AzureRmExpressRouteCircuitAuthorization** erstellt eine Schaltkreis Autorisierung, die einem Express Route-Schaltkreis hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="35c5d-106">The **New-AzureRmExpressRouteCircuitAuthorization** cmdlet creates a circuit authorization that can be added to an ExpressRoute circuit.</span></span> <span data-ttu-id="35c5d-107">Express Route-Schaltkreise verbinden Ihr lokales Netzwerk mit der Microsoft-Cloud, indem Sie einen Verbindungsanbieter anstelle des öffentlichen Internets verwenden.</span><span class="sxs-lookup"><span data-stu-id="35c5d-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="35c5d-108">Der Besitzer eines Express Route-Schaltkreises kann bis zu 10 Berechtigungen für jeden Schaltkreis erstellen. Diese Berechtigungen generieren einen Autorisierungsschlüssel, der von einem virtuellen Netzwerk Besitzer verwendet werden kann, um ein Netzwerk mit dem Schaltkreis zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="35c5d-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect a network to the circuit.</span></span> <span data-ttu-id="35c5d-109">Pro virtuelles Netzwerk kann nur eine Autorisierung vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="35c5d-109">There can only one authorization per virtual network.</span></span>

<span data-ttu-id="35c5d-110">Nachdem Sie einen Express Route-Schaltkreis erstellt haben, können Sie **Add-AzureRmExpressRouteCircuitAuthorization** verwenden, um dieser Schaltkreis eine Autorisierung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="35c5d-110">After you create an ExpressRoute circuit you can use **Add-AzureRmExpressRouteCircuitAuthorization** to add an authorization to that circuit.</span></span>
<span data-ttu-id="35c5d-111">Alternativ können Sie auch **New-AzureRmExpressRouteCircuitAuthorization** verwenden, um eine Autorisierung zu erstellen, die gleichzeitig zu einem neuen Schaltkreis hinzugefügt werden kann, wenn der Schaltkreis erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="35c5d-111">Alternatively, you can use **New-AzureRmExpressRouteCircuitAuthorization** to create an authorization that can be added to a new circuit at the same time the circuit is created.</span></span>

## <span data-ttu-id="35c5d-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="35c5d-112">EXAMPLES</span></span>

### <span data-ttu-id="35c5d-113">Beispiel 1: Erstellen einer neuen Schaltkreis Autorisierung</span><span class="sxs-lookup"><span data-stu-id="35c5d-113">Example 1: Create a new circuit authorization</span></span>
```
$Authorization = New-AzureRmExpressRouteCircuitAuthorization -Name "ContosoCircuitAuthorization"
```

<span data-ttu-id="35c5d-114">Dieser Befehl erstellt eine neue Schaltkreis Autorisierung mit dem Namen "ContosoCircuitAuthorization" und speichert dieses Objekt dann in einer Variablen mit dem Namen "$Authorization".</span><span class="sxs-lookup"><span data-stu-id="35c5d-114">This command creates a new circuit authorization named ContosoCircuitAuthorization and then stores that object in a variable named $Authorization.</span></span> <span data-ttu-id="35c5d-115">Das Speichern des Objekts in einer Variablen ist wichtig: Obwohl **New-AzureRmExpressRouteCircuitAuthorization** eine Schaltkreis Autorisierung erstellen kann, kann diese Berechtigung nicht zu einer leitungsroute hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="35c5d-115">Saving the object to a variable is important: although **New-AzureRmExpressRouteCircuitAuthorization** can create a circuit authorization it cannot add that authorization to a circuit route.</span></span> <span data-ttu-id="35c5d-116">Stattdessen wird die Variable $Authorization New-AzureRmExpressRouteCircuit beim Erstellen eines brandneuen Express Route-Schaltkreises verwendet.</span><span class="sxs-lookup"><span data-stu-id="35c5d-116">Instead, the variable $Authorization is used New-AzureRmExpressRouteCircuit when creating a brand-new ExpressRoute circuit.</span></span>

<span data-ttu-id="35c5d-117">Weitere Informationen finden Sie in der Dokumentation zum New-AzureRmExpressRouteCircuit-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35c5d-117">For more information, see the documentation for the New-AzureRmExpressRouteCircuit cmdlet.</span></span>

## <span data-ttu-id="35c5d-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="35c5d-118">PARAMETERS</span></span>

### <span data-ttu-id="35c5d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35c5d-119">-DefaultProfile</span></span>
<span data-ttu-id="35c5d-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="35c5d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35c5d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="35c5d-121">-Name</span></span>
<span data-ttu-id="35c5d-122">Gibt einen eindeutigen Namen für die neue Express Route-Schaltkreis Autorisierung an.</span><span class="sxs-lookup"><span data-stu-id="35c5d-122">Specifies a unique name for the new ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="35c5d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35c5d-123">CommonParameters</span></span>
<span data-ttu-id="35c5d-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35c5d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35c5d-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35c5d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35c5d-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="35c5d-126">INPUTS</span></span>

### <span data-ttu-id="35c5d-127">Keine</span><span class="sxs-lookup"><span data-stu-id="35c5d-127">None</span></span>
<span data-ttu-id="35c5d-128">Dieses Cmdlet akzeptiert keine Pipeline-Eingabe.</span><span class="sxs-lookup"><span data-stu-id="35c5d-128">This cmdlet does not accept pipelined input.</span></span>

## <span data-ttu-id="35c5d-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="35c5d-129">OUTPUTS</span></span>

### <span data-ttu-id="35c5d-130">PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="35c5d-130">PSExpressRouteCircuitAuthorization</span></span>
<span data-ttu-id="35c5d-131">Dieses Cmdlet erstellt Instanzen des **Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitAuthorization** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="35c5d-131">This cmdlet creates instances of the **Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization** object.</span></span>

## <span data-ttu-id="35c5d-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="35c5d-132">NOTES</span></span>

## <span data-ttu-id="35c5d-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="35c5d-133">RELATED LINKS</span></span>

[<span data-ttu-id="35c5d-134">Add-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="35c5d-134">Add-AzureRmExpressRouteCircuitAuthorization</span></span>](./Add-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="35c5d-135">Get-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="35c5d-135">Get-AzureRmExpressRouteCircuitAuthorization</span></span>](./Get-AzureRmExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="35c5d-136">Remove-AzureRmExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="35c5d-136">Remove-AzureRmExpressRouteCircuitAuthorization</span></span>](./Remove-AzureRmExpressRouteCircuitAuthorization.md)

