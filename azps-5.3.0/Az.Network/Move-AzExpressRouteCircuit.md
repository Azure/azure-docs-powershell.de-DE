---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/move-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Move-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Move-AzExpressRouteCircuit.md
ms.openlocfilehash: 2c5219e4a829ac9786b69a41afaa7362783f26b0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379572"
---
# <span data-ttu-id="dabee-101">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="dabee-101">Move-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="dabee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dabee-102">SYNOPSIS</span></span>
<span data-ttu-id="dabee-103">Verschiebt einen "ExpressRoute"-Schaltkreis aus dem klassischen Bereitstellungsmodell in das Ressourcen-Manager-Bereitstellungsmodell.</span><span class="sxs-lookup"><span data-stu-id="dabee-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

## <span data-ttu-id="dabee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dabee-104">SYNTAX</span></span>

```
Move-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> -ServiceKey <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dabee-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dabee-105">DESCRIPTION</span></span>
<span data-ttu-id="dabee-106">Das **Cmdlet Move-AzExpressRouteCircuit** verschiebt einen "ExpressRoute"-Schaltkreis aus dem klassischen Bereitstellungsmodell in das Ressourcen-Manager-Bereitstellungsmodell.</span><span class="sxs-lookup"><span data-stu-id="dabee-106">The **Move-AzExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="dabee-107">Nach dem Verschieben verhält sich der "ExpressRoute"-Schaltkreis wie jeder andere ExpressRoute-Schaltkreis, der im Ressourcen-Manager-Bereitstellungsmodell erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="dabee-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="dabee-108">Schaltkreisverbindungen, virtuelle Netzwerke und VPN-Gateways werden durch diesen Vorgang nicht verschoben.</span><span class="sxs-lookup"><span data-stu-id="dabee-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="dabee-109">Diese Ressourcen müssen nach dem Verschieben neu konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="dabee-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="dabee-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dabee-110">EXAMPLES</span></span>

### <span data-ttu-id="dabee-111">Beispiel 1: Verschieben eines ExpressRoute-Schaltkreises in das Ressourcen-Manager-Bereitstellungsmodell</span><span class="sxs-lookup"><span data-stu-id="dabee-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="dabee-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dabee-112">PARAMETERS</span></span>

### <span data-ttu-id="dabee-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dabee-113">-AsJob</span></span>
<span data-ttu-id="dabee-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="dabee-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dabee-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dabee-115">-DefaultProfile</span></span>
<span data-ttu-id="dabee-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dabee-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dabee-117">-Force</span><span class="sxs-lookup"><span data-stu-id="dabee-117">-Force</span></span>
<span data-ttu-id="dabee-118">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="dabee-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dabee-119">-Location</span><span class="sxs-lookup"><span data-stu-id="dabee-119">-Location</span></span>
<span data-ttu-id="dabee-120">Der Name des Azure-Standorts, an dem sich der "ExpressRoute"-Schaltkreis befindet.</span><span class="sxs-lookup"><span data-stu-id="dabee-120">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dabee-121">-Name</span><span class="sxs-lookup"><span data-stu-id="dabee-121">-Name</span></span>
<span data-ttu-id="dabee-122">Der Name des zu verschobenen ExpressRoute-Schaltkreises.</span><span class="sxs-lookup"><span data-stu-id="dabee-122">The name of the ExpressRoute circuit to be moved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dabee-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dabee-123">-ResourceGroupName</span></span>
<span data-ttu-id="dabee-124">Der Name der Ressourcengruppe, die den verschobenen "ExpressRoute"-Schaltkreis enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="dabee-124">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dabee-125">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="dabee-125">-ServiceKey</span></span>
<span data-ttu-id="dabee-126">Der vom ExpressRoute-Schaltkreis im klassischen Bereitstellungsmodell verwendete Dienstschlüssel.</span><span class="sxs-lookup"><span data-stu-id="dabee-126">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dabee-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="dabee-127">-Tag</span></span>
<span data-ttu-id="dabee-128">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="dabee-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="dabee-129">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="dabee-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dabee-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dabee-130">-Confirm</span></span>
<span data-ttu-id="dabee-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dabee-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dabee-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="dabee-132">-WhatIf</span></span>
<span data-ttu-id="dabee-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dabee-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dabee-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dabee-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dabee-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dabee-135">CommonParameters</span></span>
<span data-ttu-id="dabee-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dabee-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dabee-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dabee-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dabee-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dabee-138">INPUTS</span></span>

### <span data-ttu-id="dabee-139">System.String</span><span class="sxs-lookup"><span data-stu-id="dabee-139">System.String</span></span>

### <span data-ttu-id="dabee-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="dabee-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="dabee-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dabee-141">OUTPUTS</span></span>

### <span data-ttu-id="dabee-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="dabee-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="dabee-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="dabee-143">NOTES</span></span>

## <span data-ttu-id="dabee-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="dabee-144">RELATED LINKS</span></span>

[<span data-ttu-id="dabee-145">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="dabee-145">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="dabee-146">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="dabee-146">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="dabee-147">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="dabee-147">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="dabee-148">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="dabee-148">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
