---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: 0e8a4eeaad1f033377ab11d7361d71c8a63a9dc2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470144"
---
# <span data-ttu-id="abed8-101">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="abed8-101">Remove-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="abed8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abed8-102">SYNOPSIS</span></span>
<span data-ttu-id="abed8-103">Entfernt die Verbindungskonfiguration einer ExpressRoute-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="abed8-103">Removes an ExpressRoute circuit connection configuration.</span></span>

## <span data-ttu-id="abed8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="abed8-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abed8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="abed8-105">DESCRIPTION</span></span>
<span data-ttu-id="abed8-106">Das **Cmdlet "Remove-AzExpressRouteCircuitConnectionConfig"** entfernt eine ExpressRoute-Verbindungskonfiguration, die einem bestimmten Expressroutenkreis zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="abed8-106">The **Remove-AzExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="abed8-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="abed8-107">EXAMPLES</span></span>

### <span data-ttu-id="abed8-108">Beispiel 1: Entfernen einer Verbindungskonfiguration eines Schaltkreises aus einem ExpressRoute-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="abed8-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="abed8-109">Beispiel 2: Entfernen einer Verbindungskonfiguration eines Schaltkreises mithilfe von Piping aus einem ExpressRoute-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="abed8-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzExpressRouteCircuit
```

### <span data-ttu-id="abed8-110">Beispiel 3: Entfernen einer Verbindungskonfiguration eines Schaltkreises aus einem "ExpressRoute"-Schaltkreis für eine bestimmte Adressfamilie</span><span class="sxs-lookup"><span data-stu-id="abed8-110">Example 3: Remove a circuit connection configuration from an ExpressRoute circuit for a specific address family</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init -AddressPrefixType IPv4
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="abed8-111">Beispiel 4: Entfernen einer Verbindungskonfiguration eines Schaltkreises mithilfe von Piping aus einem "ExpressRoute-Schaltkreis" für eine bestimmte Adressfamilie</span><span class="sxs-lookup"><span data-stu-id="abed8-111">Example 4: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit for a specific address family</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -AddressPrefixType IPv6|Set-AzExpressRouteCircuit
```

## <span data-ttu-id="abed8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="abed8-112">PARAMETERS</span></span>

### <span data-ttu-id="abed8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abed8-113">-DefaultProfile</span></span>
<span data-ttu-id="abed8-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="abed8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="abed8-115">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="abed8-115">-ExpressRouteCircuit</span></span>
<span data-ttu-id="abed8-116">Der ExpressRoute-Schaltkreis, der die zu entfernende Peeringkonfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="abed8-116">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="abed8-117">-Name</span><span class="sxs-lookup"><span data-stu-id="abed8-117">-Name</span></span>
<span data-ttu-id="abed8-118">Der Name der Verbindungskonfiguration, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="abed8-118">The name of the circuit connection configuration to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="abed8-119">-AddressPrefixType</span><span class="sxs-lookup"><span data-stu-id="abed8-119">-AddressPrefixType</span></span>
<span data-ttu-id="abed8-120">Gibt die Adressfamilie an, die aus der Konfiguration entfernt werden muss.</span><span class="sxs-lookup"><span data-stu-id="abed8-120">Specifies the address family that needs to be removed from the config</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: IPv4 
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abed8-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="abed8-121">-Confirm</span></span>
<span data-ttu-id="abed8-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="abed8-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abed8-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="abed8-123">-WhatIf</span></span>
<span data-ttu-id="abed8-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="abed8-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="abed8-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="abed8-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abed8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abed8-126">CommonParameters</span></span>
<span data-ttu-id="abed8-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abed8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abed8-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abed8-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abed8-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="abed8-129">INPUTS</span></span>

### <span data-ttu-id="abed8-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="abed8-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="abed8-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="abed8-131">OUTPUTS</span></span>

### <span data-ttu-id="abed8-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="abed8-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="abed8-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="abed8-133">NOTES</span></span>

## <span data-ttu-id="abed8-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="abed8-134">RELATED LINKS</span></span>

[<span data-ttu-id="abed8-135">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="abed8-135">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="abed8-136">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="abed8-136">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="abed8-137">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="abed8-137">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="abed8-138">Set-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="abed8-138">Set-AzExpressRouteCircuitConnectionConfig</span></span>](Set-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="abed8-139">New-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="abed8-139">New-AzExpressRouteCircuitConnectionConfig</span></span>](New-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="abed8-140">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="abed8-140">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="abed8-141">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="abed8-141">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)