---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: cc944e06-4fa0-4ce5-88e9-ea6454b41d55
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutecircuitconnectionconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCircuitConnectionConfig.md
ms.openlocfilehash: c596dffcef97dfbb1cabbc5ca2c2455a7768c25f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100409935"
---
# <span data-ttu-id="38d18-101">Remove-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="38d18-101">Remove-AzExpressRouteCircuitConnectionConfig</span></span>

## <span data-ttu-id="38d18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38d18-102">SYNOPSIS</span></span>
<span data-ttu-id="38d18-103">Entfernt die Verbindungskonfiguration einer ExpressRoute-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="38d18-103">Removes an ExpressRoute circuit connection configuration.</span></span>

## <span data-ttu-id="38d18-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="38d18-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCircuitConnectionConfig [-Name] <String> [-ExpressRouteCircuit] <PSExpressRouteCircuit>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38d18-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="38d18-105">DESCRIPTION</span></span>
<span data-ttu-id="38d18-106">Das **Cmdlet "Remove-AzExpressRouteCircuitConnectionConfig"** entfernt eine ExpressRoute-Verbindungskonfiguration, die einem bestimmten Expressroutenkreis zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="38d18-106">The **Remove-AzExpressRouteCircuitConnectionConfig** cmdlet removes an ExpressRoute circuit connection configuration associated with a given Express Route Circuit.</span></span>

## <span data-ttu-id="38d18-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="38d18-107">EXAMPLES</span></span>

### <span data-ttu-id="38d18-108">Beispiel 1: Entfernen einer Verbindungskonfiguration eines Schaltkreises aus einem ExpressRoute-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="38d18-108">Example 1: Remove a circuit connection configuration from an ExpressRoute circuit</span></span>
```
$circuit_init = Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg
Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName -ExpressRouteCircuit $circuit_init
Set-AzExpressRouteCircuit -ExpressRouteCircuit $circuit_init
```

### <span data-ttu-id="38d18-109">Beispiel 2: Entfernen einer Verbindungskonfiguration eines Schaltkreises mithilfe von Piping aus einem ExpressRoute-Schaltkreis</span><span class="sxs-lookup"><span data-stu-id="38d18-109">Example 2: Remove a circuit connection configuration using Piping from an ExpressRoute Circuit</span></span>
```
Get-AzExpressRouteCircuit -Name $initiatingCircuitName -ResourceGroupName $rg|Remove-AzExpressRouteCircuitConnectionConfig -Name $circuitConnectionName|Set-AzExpressRouteCircuit
```

## <span data-ttu-id="38d18-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38d18-110">PARAMETERS</span></span>

### <span data-ttu-id="38d18-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38d18-111">-DefaultProfile</span></span>
<span data-ttu-id="38d18-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="38d18-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38d18-113">-ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="38d18-113">-ExpressRouteCircuit</span></span>
<span data-ttu-id="38d18-114">Der ExpressRoute-Schaltkreis, der die zu entfernende Peeringkonfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="38d18-114">The ExpressRoute circuit containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="38d18-115">-Name</span><span class="sxs-lookup"><span data-stu-id="38d18-115">-Name</span></span>
<span data-ttu-id="38d18-116">Der Name der Verbindungskonfiguration, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="38d18-116">The name of the circuit connection configuration to be removed.</span></span>

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

### <span data-ttu-id="38d18-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38d18-117">-Confirm</span></span>
<span data-ttu-id="38d18-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="38d18-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38d18-119">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="38d18-119">-WhatIf</span></span>
<span data-ttu-id="38d18-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="38d18-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="38d18-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="38d18-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38d18-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38d18-122">CommonParameters</span></span>
<span data-ttu-id="38d18-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38d18-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38d18-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38d18-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38d18-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="38d18-125">INPUTS</span></span>

### <span data-ttu-id="38d18-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="38d18-126">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="38d18-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="38d18-127">OUTPUTS</span></span>

### <span data-ttu-id="38d18-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="38d18-128">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="38d18-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="38d18-129">NOTES</span></span>

## <span data-ttu-id="38d18-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="38d18-130">RELATED LINKS</span></span>

[<span data-ttu-id="38d18-131">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="38d18-131">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="38d18-132">Get-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="38d18-132">Get-AzExpressRouteCircuitConnectionConfig</span></span>](Get-AzExpressRouteCircuitConnectionConfig.md)

[<span data-ttu-id="38d18-133">Add-AzExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="38d18-133">Add-AzExpressRouteCircuitConnectionConfig</span></span>](Add-AzExpressRouteCircuitConnectionConfig.md)





[<span data-ttu-id="38d18-134">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="38d18-134">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)

[<span data-ttu-id="38d18-135">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="38d18-135">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)
