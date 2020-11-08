---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 7c942968439d7d55fe78a3dd95c36501a2eaf10f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165814"
---
# <span data-ttu-id="7b380-101">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="7b380-101">Get-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="7b380-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7b380-102">SYNOPSIS</span></span>
<span data-ttu-id="7b380-103">Ruft Informationen zu Express Route-Schaltkreis Berechtigungen ab.</span><span class="sxs-lookup"><span data-stu-id="7b380-103">Gets information about ExpressRoute circuit authorizations.</span></span>

## <span data-ttu-id="7b380-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b380-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b380-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7b380-105">DESCRIPTION</span></span>
<span data-ttu-id="7b380-106">Das Cmdlet " **Get-AzExpressRouteCircuitAuthorization** " Ruft Informationen zu den Berechtigungen ab, die einem Express Route-Schaltkreis zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="7b380-106">The **Get-AzExpressRouteCircuitAuthorization** cmdlet gets information about the authorizations assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="7b380-107">Express Route-Schaltkreise verbinden Ihr lokales Netzwerk mit der Microsoft-Cloud, indem Sie einen Verbindungsanbieter anstelle des öffentlichen Internets verwenden.</span><span class="sxs-lookup"><span data-stu-id="7b380-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="7b380-108">Der Besitzer eines Express Route-Schaltkreises kann bis zu 10 Berechtigungen für jeden Schaltkreis erstellen. Diese Berechtigungen generieren einen Autorisierungsschlüssel, der von einem virtuellen Netzwerk Besitzer verwendet werden kann, um sein Netzwerk mit dem Schaltkreis (eine Autorisierung pro virtuelles Netzwerk) zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="7b380-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="7b380-109">Autorisierungsschlüssel sowie weitere Informationen zur Autorisierung können jederzeit angezeigt werden, indem **Sie Get-AzExpressRouteCircuitAuthorization** ausführen.</span><span class="sxs-lookup"><span data-stu-id="7b380-109">Authorization keys, as well as other information about the authorization, can be viewed at any time by running **Get-AzExpressRouteCircuitAuthorization**.</span></span>

## <span data-ttu-id="7b380-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7b380-110">EXAMPLES</span></span>

### <span data-ttu-id="7b380-111">Beispiel 1: Abrufen aller Express Route-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="7b380-111">Example 1: Get all ExpressRoute authorizations</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit
```

<span data-ttu-id="7b380-112">Diese Befehle geben Informationen zu allen Express Route-Berechtigungen zurück, die einem Express Route-Schaltkreis zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7b380-112">These commands return information about all the ExpressRoute authorizations associated with an ExpressRoute circuit.</span></span> <span data-ttu-id="7b380-113">Der erste Befehl verwendet das Cmdlet " **Get-AzExpressRouteCircuit** ", um einen Objektverweis auf einen Schaltkreis mit dem Namen ContosoCircuit zu erstellen. dieser Objektverweis wird in der Variablen $Circuit gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7b380-113">The first command uses the **Get-AzExpressRouteCircuit** cmdlet to create an object reference a circuit named ContosoCircuit; that object reference is stored in the variable $Circuit.</span></span> <span data-ttu-id="7b380-114">Der zweite Befehl verwendet dann diesen Objektverweis und das Cmdlet " **Get-AzExpressRouteCircuitAuthorization** ", um Informationen zu den Berechtigungen zurückzugeben, die mit ContosoCircuit verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="7b380-114">The second command then uses that object reference and the **Get-AzExpressRouteCircuitAuthorization** cmdlet to return information about the authorizations associated with ContosoCircuit.</span></span>

### <span data-ttu-id="7b380-115">Beispiel 2: Abrufen aller Express Route-Berechtigungen mithilfe des Where-Object-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="7b380-115">Example 2: Get all ExpressRoute authorizations using the Where-Object cmdlet</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

<span data-ttu-id="7b380-116">Diese Befehle stellen eine Variation der in Beispiel 1 verwendeten Befehle dar.</span><span class="sxs-lookup"><span data-stu-id="7b380-116">These commands represent a variation on the commands used in Example 1.</span></span> <span data-ttu-id="7b380-117">In diesem Fall werden Informationen jedoch nur für diejenigen Berechtigungen zurückgegeben, die für die Verwendung verfügbar sind (also für Berechtigungen, die nicht einem virtuellen Netzwerk zugewiesen wurden).</span><span class="sxs-lookup"><span data-stu-id="7b380-117">In this case, however, information is returned only for those authorizations that are available for use (that is, for authorizations that have not been assigned to a virtual network).</span></span> <span data-ttu-id="7b380-118">Zu diesem Zweck werden die Informationen zur Schaltkreis Autorisierung in Befehl 2 zurückgegeben und an das Cmdlet **Where-Object** umgeleitet.</span><span class="sxs-lookup"><span data-stu-id="7b380-118">To do this, the circuit authorization information is returned in command 2 and is piped to the **Where-Object** cmdlet.</span></span>
<span data-ttu-id="7b380-119">**Where-Object** wählt dann nur die Berechtigungen aus, bei denen die *AuthorizationUseStatus* -Eigenschaft auf available festgesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="7b380-119">**Where-Object** then picks out only those authorizations where the *AuthorizationUseStatus* property is set to Available.</span></span> <span data-ttu-id="7b380-120">Verwenden Sie diese Syntax für die WHERE-Klausel, um nur die nicht verfügbaren Berechtigungen aufzulisten: `{$_.AuthorizationUseStatus -ne "Available"}`</span><span class="sxs-lookup"><span data-stu-id="7b380-120">To list only those authorizations that are not available, use this syntax for the Where clause: `{$_.AuthorizationUseStatus -ne "Available"}`</span></span>

## <span data-ttu-id="7b380-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b380-121">PARAMETERS</span></span>

### <span data-ttu-id="7b380-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b380-122">-DefaultProfile</span></span>
<span data-ttu-id="7b380-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7b380-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b380-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7b380-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="7b380-125">Gibt die Express Route-Schaltkreis Autorisierung an.</span><span class="sxs-lookup"><span data-stu-id="7b380-125">Specifies the ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="7b380-126">-Name</span><span class="sxs-lookup"><span data-stu-id="7b380-126">-Name</span></span>
<span data-ttu-id="7b380-127">Gibt den Namen der Express Route-Schaltkreis Autorisierung an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="7b380-127">Specifies the name of the ExpressRoute circuit authorization that this cmdlet gets.</span></span>
<span data-ttu-id="7b380-128">-Name "ContosoCircuitAuthorization"</span><span class="sxs-lookup"><span data-stu-id="7b380-128">-Name "ContosoCircuitAuthorization"</span></span>

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

### <span data-ttu-id="7b380-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b380-129">CommonParameters</span></span>
<span data-ttu-id="7b380-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b380-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b380-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b380-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b380-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7b380-132">INPUTS</span></span>

### <span data-ttu-id="7b380-133">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7b380-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="7b380-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7b380-134">OUTPUTS</span></span>

### <span data-ttu-id="7b380-135">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="7b380-135">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="7b380-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="7b380-136">NOTES</span></span>

## <span data-ttu-id="7b380-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7b380-137">RELATED LINKS</span></span>

[<span data-ttu-id="7b380-138">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="7b380-138">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="7b380-139">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="7b380-139">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="7b380-140">Neu – AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="7b380-140">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="7b380-141">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="7b380-141">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)
