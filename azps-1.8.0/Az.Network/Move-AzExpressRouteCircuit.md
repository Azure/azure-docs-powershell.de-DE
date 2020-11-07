---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/move-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Move-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Move-AzExpressRouteCircuit.md
ms.openlocfilehash: 0ade3324e842735cab33ed6d6a40b5279cf8391e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660646"
---
# <span data-ttu-id="20e12-101">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="20e12-101">Move-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="20e12-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="20e12-102">SYNOPSIS</span></span>
<span data-ttu-id="20e12-103">Verschiebt einen Express Route-Schaltkreis vom klassischen Bereitstellungsmodell in das Bereitstellungsmodell des Ressourcen-Managers.</span><span class="sxs-lookup"><span data-stu-id="20e12-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

## <span data-ttu-id="20e12-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="20e12-104">SYNTAX</span></span>

```
Move-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> -ServiceKey <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="20e12-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20e12-105">DESCRIPTION</span></span>
<span data-ttu-id="20e12-106">Mit dem Cmdlet **Move-AzExpressRouteCircuit** wird ein Express Route-Schaltkreis vom klassischen Bereitstellungsmodell in das Bereitstellungsmodell des Ressourcen-Managers verschoben.</span><span class="sxs-lookup"><span data-stu-id="20e12-106">The **Move-AzExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="20e12-107">Nach dem Verschieben verhält sich der Express Route-Schaltkreis wie jeder andere Express Route-Schaltkreis, der im Bereitstellungsmodell des Ressourcen-Managers erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="20e12-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="20e12-108">Schaltkreis Links, virtuelle Netzwerke und VPN-Gateways werden nicht durch diesen Vorgang verschoben.</span><span class="sxs-lookup"><span data-stu-id="20e12-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="20e12-109">Diese Ressourcen müssen nach dem Umzug neu konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="20e12-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="20e12-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="20e12-110">EXAMPLES</span></span>

### <span data-ttu-id="20e12-111">Beispiel 1: Verschieben eines Express Route-Schaltkreises in das Bereitstellungsmodell des Ressourcen-Managers</span><span class="sxs-lookup"><span data-stu-id="20e12-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="20e12-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="20e12-112">PARAMETERS</span></span>

### <span data-ttu-id="20e12-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20e12-113">-AsJob</span></span>
<span data-ttu-id="20e12-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="20e12-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="20e12-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20e12-115">-DefaultProfile</span></span>
<span data-ttu-id="20e12-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="20e12-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20e12-117">-Force</span><span class="sxs-lookup"><span data-stu-id="20e12-117">-Force</span></span>
<span data-ttu-id="20e12-118">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="20e12-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="20e12-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="20e12-119">-Location</span></span>
<span data-ttu-id="20e12-120">Der Name der Azure-Position, an der sich der Express Route-Schaltkreis befindet.</span><span class="sxs-lookup"><span data-stu-id="20e12-120">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

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

### <span data-ttu-id="20e12-121">-Name</span><span class="sxs-lookup"><span data-stu-id="20e12-121">-Name</span></span>
<span data-ttu-id="20e12-122">Der Name des Express Route-Schaltkreises, der verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="20e12-122">The name of the ExpressRoute circuit to be moved.</span></span>

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

### <span data-ttu-id="20e12-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20e12-123">-ResourceGroupName</span></span>
<span data-ttu-id="20e12-124">Der Name der Ressourcengruppe, die den Express Route-Schaltkreis enthält, der verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="20e12-124">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

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

### <span data-ttu-id="20e12-125">-ServiceKey verwenden</span><span class="sxs-lookup"><span data-stu-id="20e12-125">-ServiceKey</span></span>
<span data-ttu-id="20e12-126">Der Dienstschlüssel, der vom Express Route-Schaltkreis im klassischen Bereitstellungsmodell verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="20e12-126">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

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

### <span data-ttu-id="20e12-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="20e12-127">-Tag</span></span>
<span data-ttu-id="20e12-128">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="20e12-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="20e12-129">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="20e12-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="20e12-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="20e12-130">-Confirm</span></span>
<span data-ttu-id="20e12-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="20e12-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20e12-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20e12-132">-WhatIf</span></span>
<span data-ttu-id="20e12-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="20e12-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20e12-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="20e12-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20e12-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20e12-135">CommonParameters</span></span>
<span data-ttu-id="20e12-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20e12-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20e12-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20e12-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20e12-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="20e12-138">INPUTS</span></span>

### <span data-ttu-id="20e12-139">System. String</span><span class="sxs-lookup"><span data-stu-id="20e12-139">System.String</span></span>

### <span data-ttu-id="20e12-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="20e12-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="20e12-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="20e12-141">OUTPUTS</span></span>

### <span data-ttu-id="20e12-142">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="20e12-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="20e12-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="20e12-143">NOTES</span></span>

## <span data-ttu-id="20e12-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="20e12-144">RELATED LINKS</span></span>

[<span data-ttu-id="20e12-145">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="20e12-145">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="20e12-146">Neu – AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="20e12-146">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="20e12-147">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="20e12-147">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="20e12-148">Satz-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="20e12-148">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
