---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F845ED42-A7C1-4CCC-9AD8-E9A91C3EEC7A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/move-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Move-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Move-AzExpressRouteCircuit.md
ms.openlocfilehash: 2c5219e4a829ac9786b69a41afaa7362783f26b0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300640"
---
# <span data-ttu-id="162b1-101">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="162b1-101">Move-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="162b1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="162b1-102">SYNOPSIS</span></span>
<span data-ttu-id="162b1-103">Verschiebt einen Express Route-Schaltkreis vom klassischen Bereitstellungsmodell in das Bereitstellungsmodell des Ressourcen-Managers.</span><span class="sxs-lookup"><span data-stu-id="162b1-103">Moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span>

## <span data-ttu-id="162b1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="162b1-104">SYNTAX</span></span>

```
Move-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> -ServiceKey <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="162b1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="162b1-105">DESCRIPTION</span></span>
<span data-ttu-id="162b1-106">Mit dem Cmdlet **Move-AzExpressRouteCircuit** wird ein Express Route-Schaltkreis vom klassischen Bereitstellungsmodell in das Bereitstellungsmodell des Ressourcen-Managers verschoben.</span><span class="sxs-lookup"><span data-stu-id="162b1-106">The **Move-AzExpressRouteCircuit** cmdlet moves an ExpressRoute circuit from the classic deployment model to the Resource Manager deployment model.</span></span> <span data-ttu-id="162b1-107">Nach dem Verschieben verhält sich der Express Route-Schaltkreis wie jeder andere Express Route-Schaltkreis, der im Bereitstellungsmodell des Ressourcen-Managers erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="162b1-107">After the move, the ExpressRoute circuit behaves and performs like any other ExpressRoute circuit that is created in the Resource Manager deployment model.</span></span> <span data-ttu-id="162b1-108">Schaltkreis Links, virtuelle Netzwerke und VPN-Gateways werden nicht durch diesen Vorgang verschoben.</span><span class="sxs-lookup"><span data-stu-id="162b1-108">Circuit links, virtual networks, and VPN gateways are not moved through this operation.</span></span> <span data-ttu-id="162b1-109">Diese Ressourcen müssen nach dem Umzug neu konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="162b1-109">Those resources need to be reconfigured after the move.</span></span>

## <span data-ttu-id="162b1-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="162b1-110">EXAMPLES</span></span>

### <span data-ttu-id="162b1-111">Beispiel 1: Verschieben eines Express Route-Schaltkreises in das Bereitstellungsmodell des Ressourcen-Managers</span><span class="sxs-lookup"><span data-stu-id="162b1-111">Example 1: Move an ExpressRoute circuit to the Resource Manager deployment model</span></span>
```
Move-AzExpressRouteCircuit -Name $CircuitName -ResourceGroupName $RG -Location $Location -ServiceKey $ServiceKey
```

## <span data-ttu-id="162b1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="162b1-112">PARAMETERS</span></span>

### <span data-ttu-id="162b1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="162b1-113">-AsJob</span></span>
<span data-ttu-id="162b1-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="162b1-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="162b1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="162b1-115">-DefaultProfile</span></span>
<span data-ttu-id="162b1-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="162b1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="162b1-117">-Force</span><span class="sxs-lookup"><span data-stu-id="162b1-117">-Force</span></span>
<span data-ttu-id="162b1-118">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="162b1-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="162b1-119">-Standort</span><span class="sxs-lookup"><span data-stu-id="162b1-119">-Location</span></span>
<span data-ttu-id="162b1-120">Der Name der Azure-Position, an der sich der Express Route-Schaltkreis befindet.</span><span class="sxs-lookup"><span data-stu-id="162b1-120">The name of the Azure location where the ExpressRoute circuit resides.</span></span>

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

### <span data-ttu-id="162b1-121">-Name</span><span class="sxs-lookup"><span data-stu-id="162b1-121">-Name</span></span>
<span data-ttu-id="162b1-122">Der Name des Express Route-Schaltkreises, der verschoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="162b1-122">The name of the ExpressRoute circuit to be moved.</span></span>

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

### <span data-ttu-id="162b1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="162b1-123">-ResourceGroupName</span></span>
<span data-ttu-id="162b1-124">Der Name der Ressourcengruppe, die den Express Route-Schaltkreis enthält, der verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="162b1-124">The name of the resource group that will contain the ExpressRoute circuit being moved.</span></span>

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

### <span data-ttu-id="162b1-125">-ServiceKey verwenden</span><span class="sxs-lookup"><span data-stu-id="162b1-125">-ServiceKey</span></span>
<span data-ttu-id="162b1-126">Der Dienstschlüssel, der vom Express Route-Schaltkreis im klassischen Bereitstellungsmodell verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="162b1-126">The Service Key used by the ExpressRoute circuit in the classic deployment model.</span></span>

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

### <span data-ttu-id="162b1-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="162b1-127">-Tag</span></span>
<span data-ttu-id="162b1-128">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="162b1-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="162b1-129">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="162b1-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="162b1-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="162b1-130">-Confirm</span></span>
<span data-ttu-id="162b1-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="162b1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="162b1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="162b1-132">-WhatIf</span></span>
<span data-ttu-id="162b1-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="162b1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="162b1-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="162b1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="162b1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="162b1-135">CommonParameters</span></span>
<span data-ttu-id="162b1-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="162b1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="162b1-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="162b1-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="162b1-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="162b1-138">INPUTS</span></span>

### <span data-ttu-id="162b1-139">System. String</span><span class="sxs-lookup"><span data-stu-id="162b1-139">System.String</span></span>

### <span data-ttu-id="162b1-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="162b1-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="162b1-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="162b1-141">OUTPUTS</span></span>

### <span data-ttu-id="162b1-142">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="162b1-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="162b1-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="162b1-143">NOTES</span></span>

## <span data-ttu-id="162b1-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="162b1-144">RELATED LINKS</span></span>

[<span data-ttu-id="162b1-145">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="162b1-145">Get-AzExpressRouteCircuit</span></span>](./Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="162b1-146">Neu – AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="162b1-146">New-AzExpressRouteCircuit</span></span>](./New-AzExpressRouteCircuit.md)

[<span data-ttu-id="162b1-147">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="162b1-147">Remove-AzExpressRouteCircuit</span></span>](./Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="162b1-148">Satz-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="162b1-148">Set-AzExpressRouteCircuit</span></span>](./Set-AzExpressRouteCircuit.md)
