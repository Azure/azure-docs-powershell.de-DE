---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 2c58549ee79cd24d29c1e3549d729995313c5748
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926539"
---
# <span data-ttu-id="2e91f-101">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="2e91f-101">Get-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="2e91f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e91f-102">SYNOPSIS</span></span>
<span data-ttu-id="2e91f-103">Ruft Informationen zu ExpressRoute-Schaltkreisautorisierungen ab.</span><span class="sxs-lookup"><span data-stu-id="2e91f-103">Gets information about ExpressRoute circuit authorizations.</span></span>

## <span data-ttu-id="2e91f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2e91f-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e91f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2e91f-105">DESCRIPTION</span></span>
<span data-ttu-id="2e91f-106">Das **Get-AzExpressRouteCircuitAuthorization-Cmdlet** ruft Informationen zu den Berechtigungen ab, die einem ExpressRoute-Schaltkreis zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="2e91f-106">The **Get-AzExpressRouteCircuitAuthorization** cmdlet gets information about the authorizations assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="2e91f-107">ExpressRoute-Schaltkreise verbinden Ihr lokales Netzwerk mit der Microsoft-Cloud, indem sie einen Konnektivitätsanbieter anstelle des öffentlichen Internets verwenden.</span><span class="sxs-lookup"><span data-stu-id="2e91f-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="2e91f-108">Der Besitzer eines #A0 kann bis zu 10 Berechtigungen für jeden Schaltkreis erstellen. Diese Autorisierungen generieren einen Autorisierungsschlüssel, der von einem Besitzer des virtuellen Netzwerks verwendet werden kann, um sein Netzwerk mit dem Schaltkreis zu verbinden (eine Autorisierung pro virtuellem Netzwerk).</span><span class="sxs-lookup"><span data-stu-id="2e91f-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="2e91f-109">Autorisierungsschlüssel sowie andere Informationen zur Autorisierung können jederzeit angezeigt werden, indem **Get-AzExpressRouteCircuitAuthorization ausgeführt wird.**</span><span class="sxs-lookup"><span data-stu-id="2e91f-109">Authorization keys, as well as other information about the authorization, can be viewed at any time by running **Get-AzExpressRouteCircuitAuthorization**.</span></span>

## <span data-ttu-id="2e91f-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2e91f-110">EXAMPLES</span></span>

### <span data-ttu-id="2e91f-111">Beispiel 1: Alle ExpressRoute-Berechtigungen erhalten</span><span class="sxs-lookup"><span data-stu-id="2e91f-111">Example 1: Get all ExpressRoute authorizations</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit
```

<span data-ttu-id="2e91f-112">Diese Befehle geben Informationen zu allen ExpressRoute-Berechtigungen zurück, die einem ExpressRoute-Schaltkreis zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="2e91f-112">These commands return information about all the ExpressRoute authorizations associated with an ExpressRoute circuit.</span></span> <span data-ttu-id="2e91f-113">Der erste Befehl verwendet das **Get-AzExpressRouteCircuit-Cmdlet,** um einen Objektverweis auf einen Schaltkreis namens ContosoCircuit zu erstellen. der Objektverweis in der Variablen-$Circuit.</span><span class="sxs-lookup"><span data-stu-id="2e91f-113">The first command uses the **Get-AzExpressRouteCircuit** cmdlet to create an object reference a circuit named ContosoCircuit; that object reference is stored in the variable $Circuit.</span></span> <span data-ttu-id="2e91f-114">Der zweite Befehl verwendet dann diesen Objektverweis und das **Get-AzExpressRouteCircuitAuthorization-Cmdlet,** um Informationen zu den Berechtigungen zurückgibt, die ContosoCircuit zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="2e91f-114">The second command then uses that object reference and the **Get-AzExpressRouteCircuitAuthorization** cmdlet to return information about the authorizations associated with ContosoCircuit.</span></span>

### <span data-ttu-id="2e91f-115">Beispiel 2: Alle ExpressRoute-Autorisierungen mithilfe des Where-Object erhalten</span><span class="sxs-lookup"><span data-stu-id="2e91f-115">Example 2: Get all ExpressRoute authorizations using the Where-Object cmdlet</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

<span data-ttu-id="2e91f-116">Diese Befehle stellen eine Variation der in Beispiel 1 verwendeten Befehle dar.</span><span class="sxs-lookup"><span data-stu-id="2e91f-116">These commands represent a variation on the commands used in Example 1.</span></span> <span data-ttu-id="2e91f-117">In diesem Fall werden informationen jedoch nur für die Autorisierungen zurückgegeben, die für die Verwendung verfügbar sind (d. h. für Autorisierungen, die nicht einem virtuellen Netzwerk zugewiesen wurden).</span><span class="sxs-lookup"><span data-stu-id="2e91f-117">In this case, however, information is returned only for those authorizations that are available for use (that is, for authorizations that have not been assigned to a virtual network).</span></span> <span data-ttu-id="2e91f-118">Zu diesem Grund werden die Informationen zur Schaltungsautorisierung in Befehl 2 zurückgegeben und an das **Cmdlet Where-Object** pipedlet weiterverrohrt.</span><span class="sxs-lookup"><span data-stu-id="2e91f-118">To do this, the circuit authorization information is returned in command 2 and is piped to the **Where-Object** cmdlet.</span></span>
<span data-ttu-id="2e91f-119">**Where-Object** wählt dann nur die Berechtigungen aus, bei denen die *AuthorizationUseStatus-Eigenschaft* auf Verfügbar festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="2e91f-119">**Where-Object** then picks out only those authorizations where the *AuthorizationUseStatus* property is set to Available.</span></span> <span data-ttu-id="2e91f-120">Wenn Sie nur die nicht verfügbaren Berechtigungen auflisten möchten, verwenden Sie diese Syntax für die Where-Klausel: `{$_.AuthorizationUseStatus -ne "Available"}`</span><span class="sxs-lookup"><span data-stu-id="2e91f-120">To list only those authorizations that are not available, use this syntax for the Where clause: `{$_.AuthorizationUseStatus -ne "Available"}`</span></span>

## <span data-ttu-id="2e91f-121">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2e91f-121">PARAMETERS</span></span>

### <span data-ttu-id="2e91f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e91f-122">-DefaultProfile</span></span>
<span data-ttu-id="2e91f-123">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2e91f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e91f-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2e91f-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="2e91f-125">Gibt die ExpressRoute-Schaltkreisautorisierung an.</span><span class="sxs-lookup"><span data-stu-id="2e91f-125">Specifies the ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="2e91f-126">-Name</span><span class="sxs-lookup"><span data-stu-id="2e91f-126">-Name</span></span>
<span data-ttu-id="2e91f-127">Gibt den Namen der ExpressRoute-Schaltkreisautorisierung an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="2e91f-127">Specifies the name of the ExpressRoute circuit authorization that this cmdlet gets.</span></span>
<span data-ttu-id="2e91f-128">-Name "ContosoCircuitAuthorization"</span><span class="sxs-lookup"><span data-stu-id="2e91f-128">-Name "ContosoCircuitAuthorization"</span></span>

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

### <span data-ttu-id="2e91f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e91f-129">CommonParameters</span></span>
<span data-ttu-id="2e91f-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e91f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e91f-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e91f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e91f-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2e91f-132">INPUTS</span></span>

### <span data-ttu-id="2e91f-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2e91f-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="2e91f-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2e91f-134">OUTPUTS</span></span>

### <span data-ttu-id="2e91f-135">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="2e91f-135">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="2e91f-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2e91f-136">NOTES</span></span>

## <span data-ttu-id="2e91f-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2e91f-137">RELATED LINKS</span></span>

[<span data-ttu-id="2e91f-138">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="2e91f-138">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="2e91f-139">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2e91f-139">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="2e91f-140">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="2e91f-140">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="2e91f-141">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="2e91f-141">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)
