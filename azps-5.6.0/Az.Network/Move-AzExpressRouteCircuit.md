---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: https://docs.microsoft.com/powershell/module/az.network/move-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Move-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Move-AzExpressRouteCircuit.md
ms.openlocfilehash: 6964767438fac6a1afd8da4333560f49cfe1bb44
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918715"
---
# <span data-ttu-id="87c93-101">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="87c93-101">Move-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="87c93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87c93-102">SYNOPSIS</span></span>
<span data-ttu-id="87c93-103">Verschiebt einen ExpressRoute-Schaltkreis vom klassischen Bereitstellungsmodell in das Ressourcen-Manager-Bereitstellungsmodell.</span><span class="sxs-lookup"><span data-stu-id="87c93-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

## <span data-ttu-id="87c93-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="87c93-104">SYNTAX</span></span>

```
Move-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> -ServiceKey <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="87c93-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="87c93-105">DESCRIPTION</span></span>
<span data-ttu-id="87c93-106">Das **Move-AzExpressRouteCircuit-Cmdlet** verschiebt einen ExpressRoute-Schaltkreis vom klassischen Bereitstellungsmodell in das Ressourcen-Manager-Bereitstellungsmodell.</span><span class="sxs-lookup"><span data-stu-id="87c93-106">The **Move-AzExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="87c93-107">Nach dem Verschieben verhält sich der ExpressRoute-Schaltkreis wie jeder andere ExpressRoute-Schaltkreis, der im Ressourcen-Manager-Bereitstellungsmodell erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="87c93-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="87c93-108">Schaltkreisverbindungen, virtuelle Netzwerke und VPN-Gateways werden durch diesen Vorgang nicht verschoben.</span><span class="sxs-lookup"><span data-stu-id="87c93-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="87c93-109">Diese Ressourcen müssen nach dem Verschieben neu konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="87c93-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="87c93-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="87c93-110">EXAMPLES</span></span>

### <span data-ttu-id="87c93-111">Beispiel 1: Verschieben eines ExpressRoute-Schaltkreises in das Ressourcen-Manager-Bereitstellungsmodell</span><span class="sxs-lookup"><span data-stu-id="87c93-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="87c93-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="87c93-112">PARAMETERS</span></span>

### <span data-ttu-id="87c93-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="87c93-113">-AsJob</span></span>
<span data-ttu-id="87c93-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="87c93-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="87c93-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87c93-115">-DefaultProfile</span></span>
<span data-ttu-id="87c93-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="87c93-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87c93-117">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="87c93-117">-Force</span></span>
<span data-ttu-id="87c93-118">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="87c93-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="87c93-119">-Location</span><span class="sxs-lookup"><span data-stu-id="87c93-119">-Location</span></span>
<span data-ttu-id="87c93-120">Der Name des Azure-Speicherorts, an dem sich der ExpressRoute-Schaltkreis befindet.</span><span class="sxs-lookup"><span data-stu-id="87c93-120">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

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

### <span data-ttu-id="87c93-121">-Name</span><span class="sxs-lookup"><span data-stu-id="87c93-121">-Name</span></span>
<span data-ttu-id="87c93-122">Der Name des zu verschobenen ExpressRoute-Schaltkreises.</span><span class="sxs-lookup"><span data-stu-id="87c93-122">The name of the ExpressRoute circuit to be moved.</span></span>

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

### <span data-ttu-id="87c93-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87c93-123">-ResourceGroupName</span></span>
<span data-ttu-id="87c93-124">Der Name der Ressourcengruppe, die den verschobenen ExpressRoute-Schaltkreis enthält.</span><span class="sxs-lookup"><span data-stu-id="87c93-124">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

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

### <span data-ttu-id="87c93-125">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="87c93-125">-ServiceKey</span></span>
<span data-ttu-id="87c93-126">Der vom ExpressRoute-Schaltkreis im klassischen Bereitstellungsmodell verwendete Dienstschlüssel.</span><span class="sxs-lookup"><span data-stu-id="87c93-126">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

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

### <span data-ttu-id="87c93-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="87c93-127">-Tag</span></span>
<span data-ttu-id="87c93-128">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="87c93-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="87c93-129">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="87c93-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="87c93-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="87c93-130">-Confirm</span></span>
<span data-ttu-id="87c93-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="87c93-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87c93-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87c93-132">-WhatIf</span></span>
<span data-ttu-id="87c93-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="87c93-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87c93-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="87c93-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87c93-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87c93-135">CommonParameters</span></span>
<span data-ttu-id="87c93-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87c93-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87c93-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87c93-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87c93-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="87c93-138">INPUTS</span></span>

### <span data-ttu-id="87c93-139">System.String</span><span class="sxs-lookup"><span data-stu-id="87c93-139">System.String</span></span>

### <span data-ttu-id="87c93-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="87c93-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="87c93-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="87c93-141">OUTPUTS</span></span>

### <span data-ttu-id="87c93-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="87c93-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="87c93-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="87c93-143">NOTES</span></span>

## <span data-ttu-id="87c93-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="87c93-144">RELATED LINKS</span></span>

[<span data-ttu-id="87c93-145">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="87c93-145">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="87c93-146">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="87c93-146">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="87c93-147">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="87c93-147">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="87c93-148">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="87c93-148">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
