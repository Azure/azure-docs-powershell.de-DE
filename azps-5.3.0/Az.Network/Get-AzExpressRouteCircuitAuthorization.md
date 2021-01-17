---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D80F94B-AF9D-40C2-BE7E-2F32E5E926D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressroutecircuitauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCircuitAuthorization.md
ms.openlocfilehash: 7c942968439d7d55fe78a3dd95c36501a2eaf10f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458875"
---
# <span data-ttu-id="36359-101">Get-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="36359-101">Get-AzExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="36359-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36359-102">SYNOPSIS</span></span>
<span data-ttu-id="36359-103">Ruft Informationen zu den Berechtigungen für den ExpressRoute-Schaltkreis ab.</span><span class="sxs-lookup"><span data-stu-id="36359-103">Gets information about ExpressRoute circuit authorizations.</span></span>

## <span data-ttu-id="36359-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="36359-104">SYNTAX</span></span>

```
Get-AzExpressRouteCircuitAuthorization [-Name <String>] -ExpressRouteCircuit <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36359-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="36359-105">DESCRIPTION</span></span>
<span data-ttu-id="36359-106">Das **Cmdlet "Get-AzExpressRouteCircuitAuthorization"** ruft Informationen zu den Berechtigungen ab, die einem ExpressRoute-Schaltkreis zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="36359-106">The **Get-AzExpressRouteCircuitAuthorization** cmdlet gets information about the authorizations assigned to an ExpressRoute circuit.</span></span> <span data-ttu-id="36359-107">ExpressRoute-Schaltkreise verbinden Ihr lokales Netzwerk mit der Microsoft-Cloud, indem anstelle des öffentlichen Internets ein Konnektivitätsanbieter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="36359-107">ExpressRoute circuits connect your on-premises network to the Microsoft cloud by using a connectivity provider instead of the public Internet.</span></span> <span data-ttu-id="36359-108">Der Besitzer eines #A0 kann bis zu 10 Autorisierungen für jeden Schaltkreis erstellen. diese Autorisierungen generieren einen Autorisierungsschlüssel, der von einem virtuellen Netzwerkbesitzer verwendet werden kann, um sein Netzwerk mit dem Schaltkreis zu verbinden (eine Autorisierung pro virtuellem Netzwerk).</span><span class="sxs-lookup"><span data-stu-id="36359-108">The owner of an ExpressRoute circuit can create as many as 10 authorizations for each circuit; these authorizations generate an authorization key that can be used by a virtual network owner to connect his or her network to the circuit (one authorization per virtual network).</span></span> <span data-ttu-id="36359-109">Autorisierungsschlüssel sowie andere Informationen zur Autorisierung können jederzeit angezeigt werden, indem Sie **"Get-AzExpressRouteCircuitAuthorization" ausführen.**</span><span class="sxs-lookup"><span data-stu-id="36359-109">Authorization keys, as well as other information about the authorization, can be viewed at any time by running **Get-AzExpressRouteCircuitAuthorization**.</span></span>

## <span data-ttu-id="36359-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="36359-110">EXAMPLES</span></span>

### <span data-ttu-id="36359-111">Beispiel 1: Erhalten aller ExpressRoute-Autorisierungen</span><span class="sxs-lookup"><span data-stu-id="36359-111">Example 1: Get all ExpressRoute authorizations</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit
```

<span data-ttu-id="36359-112">Diese Befehle geben Informationen zu allen ExpressRoute-Autorisierungen zurück, die einem ExpressRoute-Schaltkreis zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="36359-112">These commands return information about all the ExpressRoute authorizations associated with an ExpressRoute circuit.</span></span> <span data-ttu-id="36359-113">Der erste Befehl verwendet das **Cmdlet "Get-AzExpressRouteCircuit",** um einen Objektverweis auf einen Schaltkreis namens "ContosoCircuit" zu erstellen. objektverweis in der Variablen gespeichert $Circuit.</span><span class="sxs-lookup"><span data-stu-id="36359-113">The first command uses the **Get-AzExpressRouteCircuit** cmdlet to create an object reference a circuit named ContosoCircuit; that object reference is stored in the variable $Circuit.</span></span> <span data-ttu-id="36359-114">Der zweite Befehl verwendet dann diesen Objektverweis und das **Cmdlet "Get-AzExpressRouteCircuitAuthorization",** um Informationen zu den Autorisierungen zurückgibt, die ContosoCircuit zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="36359-114">The second command then uses that object reference and the **Get-AzExpressRouteCircuitAuthorization** cmdlet to return information about the authorizations associated with ContosoCircuit.</span></span>

### <span data-ttu-id="36359-115">Beispiel 2: Erhalten aller ExpressRoute-Autorisierungen mithilfe des Where-Object Cmdlets</span><span class="sxs-lookup"><span data-stu-id="36359-115">Example 2: Get all ExpressRoute authorizations using the Where-Object cmdlet</span></span>
```
$Circuit = Get-AzExpressRouteCircuit -Name "ContosoCircuit" -ResourceGroupName "ContosoResourceGroup"
 Get-AzExpressRouteCircuitAuthorization -Circuit $Circuit | Where-Object {$_.AuthorizationUseStatus -eq "Available"}
```

<span data-ttu-id="36359-116">Diese Befehle stellen eine Variation der in Beispiel 1 verwendeten Befehle dar.</span><span class="sxs-lookup"><span data-stu-id="36359-116">These commands represent a variation on the commands used in Example 1.</span></span> <span data-ttu-id="36359-117">In diesem Fall werden informationen jedoch nur für die Autorisierungen zurückgegeben, die zur Verwendung zur Verfügung stehen (d. h. für Autorisierungen, die keinem virtuellen Netzwerk zugewiesen wurden).</span><span class="sxs-lookup"><span data-stu-id="36359-117">In this case, however, information is returned only for those authorizations that are available for use (that is, for authorizations that have not been assigned to a virtual network).</span></span> <span data-ttu-id="36359-118">Dazu werden die Informationen zur Schaltkreisautorisierung in Befehl 2 zurückgegeben und an das **Cmdlet "Where-Object"** weitergeseniert.</span><span class="sxs-lookup"><span data-stu-id="36359-118">To do this, the circuit authorization information is returned in command 2 and is piped to the **Where-Object** cmdlet.</span></span>
<span data-ttu-id="36359-119">**Where-Object wählt** dann nur die Autorisierungen aus, für die die *Eigenschaft "AuthorizationUseStatus"* auf "Verfügbar" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="36359-119">**Where-Object** then picks out only those authorizations where the *AuthorizationUseStatus* property is set to Available.</span></span> <span data-ttu-id="36359-120">Wenn Sie nur die nicht verfügbaren Autorisierungen auflisten möchten, verwenden Sie die folgende Syntax für die Where-Klausel: `{$_.AuthorizationUseStatus -ne "Available"}`</span><span class="sxs-lookup"><span data-stu-id="36359-120">To list only those authorizations that are not available, use this syntax for the Where clause: `{$_.AuthorizationUseStatus -ne "Available"}`</span></span>

## <span data-ttu-id="36359-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36359-121">PARAMETERS</span></span>

### <span data-ttu-id="36359-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36359-122">-DefaultProfile</span></span>
<span data-ttu-id="36359-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="36359-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36359-124">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="36359-124">-ExpressRouteCircuit</span></span>
<span data-ttu-id="36359-125">Gibt die Autorisierung des ExpressRoute-Schaltkreises an.</span><span class="sxs-lookup"><span data-stu-id="36359-125">Specifies the ExpressRoute circuit authorization.</span></span>

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

### <span data-ttu-id="36359-126">-Name</span><span class="sxs-lookup"><span data-stu-id="36359-126">-Name</span></span>
<span data-ttu-id="36359-127">Gibt den Namen der Autorisierung des ExpressRoute-Schaltkreises an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="36359-127">Specifies the name of the ExpressRoute circuit authorization that this cmdlet gets.</span></span>
<span data-ttu-id="36359-128">-Name "ContosoCircuitAuthorization"</span><span class="sxs-lookup"><span data-stu-id="36359-128">-Name "ContosoCircuitAuthorization"</span></span>

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

### <span data-ttu-id="36359-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36359-129">CommonParameters</span></span>
<span data-ttu-id="36359-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36359-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36359-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36359-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36359-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="36359-132">INPUTS</span></span>

### <span data-ttu-id="36359-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="36359-133">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="36359-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="36359-134">OUTPUTS</span></span>

### <span data-ttu-id="36359-135">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="36359-135">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization</span></span>

## <span data-ttu-id="36359-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="36359-136">NOTES</span></span>

## <span data-ttu-id="36359-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="36359-137">RELATED LINKS</span></span>

[<span data-ttu-id="36359-138">Add-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="36359-138">Add-AzExpressRouteCircuitAuthorization</span></span>](./Add-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="36359-139">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="36359-139">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="36359-140">New-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="36359-140">New-AzExpressRouteCircuitAuthorization</span></span>](./New-AzExpressRouteCircuitAuthorization.md)

[<span data-ttu-id="36359-141">Remove-AzExpressRouteCircuitAuthorization</span><span class="sxs-lookup"><span data-stu-id="36359-141">Remove-AzExpressRouteCircuitAuthorization</span></span>](./Remove-AzExpressRouteCircuitAuthorization.md)
